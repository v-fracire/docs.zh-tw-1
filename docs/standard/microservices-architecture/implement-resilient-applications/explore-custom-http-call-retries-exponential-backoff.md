---
title: 使用指數輪詢探索自訂 HTTP 呼叫重試
description: 了解如何使用指數輪詢從頭開始實作 HTTP 呼叫重試，以處理可能發生的HTTP 失敗案例。
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/08/2018
ms.openlocfilehash: c323b8c4e783ed18c601562cfb25e1ca4986d499
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/06/2018
ms.locfileid: "37878613"
---
# <a name="explore-custom-http-call-retries-with-exponential-backoff"></a><span data-ttu-id="b18c6-103">使用指數輪詢探索自訂 HTTP 呼叫重試</span><span class="sxs-lookup"><span data-stu-id="b18c6-103">Explore custom HTTP call retries with exponential backoff</span></span>

<span data-ttu-id="b18c6-104">若要建立具復原功能的微服務，您必須處理可能的 HTTP 失敗案例。</span><span class="sxs-lookup"><span data-stu-id="b18c6-104">To create resilient microservices, you need to handle possible HTTP failure scenarios.</span></span> <span data-ttu-id="b18c6-105">處理這些失敗的一種方式 (雖然不建議使用) 是使用指數輪詢建立您自己的重試實作。</span><span class="sxs-lookup"><span data-stu-id="b18c6-105">One way of handling those failures, although not recommended, is to create your own implementation of retries with exponential backoff.</span></span>

<span data-ttu-id="b18c6-106">**重要事項：** 本節將說明如何建立您自己自訂的程式碼來實作 HTTP 呼叫重試。</span><span class="sxs-lookup"><span data-stu-id="b18c6-106">**Important note:** This section shows you how you could create your own custom code to implement HTTP call retries.</span></span> <span data-ttu-id="b18c6-107">不過，不建議您自己做，而是使用功能更強大且可靠，同時使用方式更簡單的機制，例如，使用自 .NET Core 2.1 開始提供的 `HttpClientFactory` 搭配 Polly。</span><span class="sxs-lookup"><span data-stu-id="b18c6-107">However, it is not recommended to do it by your own but to use more powerful and reliable while simpler to use mechanisms, such as `HttpClientFactory` with Polly, available since .NET Core 2.1.</span></span> <span data-ttu-id="b18c6-108">這些建議方法會在後續各節中說明。</span><span class="sxs-lookup"><span data-stu-id="b18c6-108">Those recommended approaches are explained in the next sections.</span></span> 

<span data-ttu-id="b18c6-109">一開始探索時，您可以實作自己的程式碼來包含指數輪詢的公用程式類別，如 [RetryWithExponentialBackoff.cs](https://gist.github.com/CESARDELATORRE/6d7f647b29e55fdc219ee1fd2babb260) 中所示，再加上類似如下的程式碼 ([GitHub 存放庫](https://gist.github.com/CESARDELATORRE/d80c6423a1aebaffaf387469f5194f5b)中也有提供)。</span><span class="sxs-lookup"><span data-stu-id="b18c6-109">As an initial exploration, you could implement your own code with a utility class for exponential backoff as in [RetryWithExponentialBackoff.cs](https://gist.github.com/CESARDELATORRE/6d7f647b29e55fdc219ee1fd2babb260), plus code like the following (which is also available at this [GitHub repo](https://gist.github.com/CESARDELATORRE/d80c6423a1aebaffaf387469f5194f5b)).</span></span>

```csharp
public sealed class RetryWithExponentialBackoff
{
    private readonly int maxRetries, delayMilliseconds, maxDelayMilliseconds;

    public RetryWithExponentialBackoff(int maxRetries = 50,
        int delayMilliseconds = 200,
        int maxDelayMilliseconds = 2000)
    {
        this.maxRetries = maxRetries;
        this.delayMilliseconds = delayMilliseconds;
        this.maxDelayMilliseconds = maxDelayMilliseconds;
    }

    public async Task RunAsync(Func<Task> func)
    {
        ExponentialBackoff backoff = new ExponentialBackoff(this.maxRetries,
            this.delayMilliseconds,
            this.maxDelayMilliseconds);
        retry:
        try
        {
            await func();
        }
        catch (Exception ex) when (ex is TimeoutException ||
            ex is System.Net.Http.HttpRequestException)
        {
            Debug.WriteLine("Exception raised is: " +
                ex.GetType().ToString() +
                " –Message: " + ex.Message +
                " -- Inner Message: " +
                ex.InnerException.Message);
            await backoff.Delay();
            goto retry;
        }
    }
}

public struct ExponentialBackoff
{
    private readonly int m_maxRetries, m_delayMilliseconds, m_maxDelayMilliseconds;
    private int m_retries, m_pow;

    public ExponentialBackoff(int maxRetries, int delayMilliseconds,
        int maxDelayMilliseconds)
    {
        m_maxRetries = maxRetries;
        m_delayMilliseconds = delayMilliseconds;
        m_maxDelayMilliseconds = maxDelayMilliseconds;
        m_retries = 0;
        m_pow = 1;
    }

    public Task Delay()
    {
        if (m_retries == m_maxRetries)
        {
            throw new TimeoutException("Max retry attempts exceeded.");
        }
        ++m_retries;
        if (m_retries < 31)
        {
            m_pow = m_pow << 1; // m_pow = Pow(2, m_retries - 1)
        }
        int delay = Math.Min(m_delayMilliseconds * (m_pow - 1) / 2,
            m_maxDelayMilliseconds);
        return Task.Delay(delay);
    }
}
```

<span data-ttu-id="b18c6-110">在用戶端 C\# 應用程式 (另一個 Web API 用戶端微服務、ASP.NET MVC 應用程式或甚至 C\# Xamarin 應用程式) 中使用此程式碼相當簡單。</span><span class="sxs-lookup"><span data-stu-id="b18c6-110">Using this code in a client C\# application (another Web API client microservice, an ASP.NET MVC application, or even a C\# Xamarin application) is straightforward.</span></span> <span data-ttu-id="b18c6-111">下列範例示範如何使用 HttpClient 類別。</span><span class="sxs-lookup"><span data-stu-id="b18c6-111">The following example shows how, using the HttpClient class.</span></span>

```csharp
public async Task<Catalog> GetCatalogItems(int page,int take, int? brand, int? type)
{
    _apiClient = new HttpClient();
    var itemsQs = $"items?pageIndex={page}&pageSize={take}";
    var filterQs = "";
    var catalogUrl = $"{_remoteServiceBaseUrl}items{filterQs}?pageIndex={page}&pageSize={take}";
    var dataString = "";
    //
    // Using HttpClient with Retry and Exponential Backoff
    //
    var retry = new RetryWithExponentialBackoff();
    await retry.RunAsync(async () =>
    {
        // work with HttpClient call
        dataString = await _apiClient.GetStringAsync(catalogUrl);
    });
    return JsonConvert.DeserializeObject<Catalog>(dataString);
}
```

<span data-ttu-id="b18c6-112">請記住，此程式碼只適合作為概念證明。</span><span class="sxs-lookup"><span data-stu-id="b18c6-112">Remember that this code is suitable only as a proof of concept.</span></span> <span data-ttu-id="b18c6-113">後續各節說明如何使用 HttpClientFactory 這個縝密但使用方式更簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="b18c6-113">The next sections explain how to use more sophisticated approaches while simpler, by using HttpClientFactory.</span></span>
<span data-ttu-id="b18c6-114">HttpClientFactory 自.NET Core 2.1 開始提供，它內含像 Polly 一樣經過實證的復原程式庫。</span><span class="sxs-lookup"><span data-stu-id="b18c6-114">HttpClientFactory is available since .NET Core 2.1, with proven resiliency libraries like Polly.</span></span> 


>[!div class="step-by-step"]
<span data-ttu-id="b18c6-115">[上一頁](implement-resilient-entity-framework-core-sql-connections.md)
[下一頁](use-httpclientfactory-to-implement-resilient-http-requests.md)</span><span class="sxs-lookup"><span data-stu-id="b18c6-115">[Previous](implement-resilient-entity-framework-core-sql-connections.md)
[Next](use-httpclientfactory-to-implement-resilient-http-requests.md)</span></span>