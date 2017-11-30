---
title: "SingleTagSectionHandler 自訂項目"
ms.date: 05/01/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: article
f1_keywords: http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName
helpviewer_keywords: custom element
ms.assetid: e62056c6-b351-40eb-afc0-cc13fc44e45e
author: guardrex
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 496967bc3638344d2b39d428b85270b575b325ed
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="custom-element-for-singletagsectionhandler"></a><span data-ttu-id="2beb7-102">SingleTagSectionHandler 自訂項目</span><span class="sxs-lookup"><span data-stu-id="2beb7-102">Custom element for SingleTagSectionHandler</span></span>

<span data-ttu-id="2beb7-103">定義中所定義的自訂組態區段的設定</span><span class="sxs-lookup"><span data-stu-id="2beb7-103">Defines settings in a custom configuration section that is defined by a</span></span> <section> <span data-ttu-id="2beb7-104">項目，並使用<xref:System.Configuration.SingleTagSectionHandler>類別。</span><span class="sxs-lookup"><span data-stu-id="2beb7-104">element and uses the <xref:System.Configuration.SingleTagSectionHandler> class.</span></span>

<span data-ttu-id="2beb7-105">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="2beb7-105">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="2beb7-106">&nbsp;&nbsp;*\<sectionName >*</span><span class="sxs-lookup"><span data-stu-id="2beb7-106">&nbsp;&nbsp;*\<sectionName>*</span></span>

## <a name="syntax"></a><span data-ttu-id="2beb7-107">語法</span><span class="sxs-lookup"><span data-stu-id="2beb7-107">Syntax</span></span>

```xml
<sectionName key="value" key2="value2" ... />
```

## <a name="attributes"></a><span data-ttu-id="2beb7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2beb7-108">Attributes</span></span>

<span data-ttu-id="2beb7-109">屬性和屬性值是使用者定義。</span><span class="sxs-lookup"><span data-stu-id="2beb7-109">Attributes and attribute values are user defined.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2beb7-110">父項目</span><span class="sxs-lookup"><span data-stu-id="2beb7-110">Parent element</span></span>

|     | <span data-ttu-id="2beb7-111">說明</span><span class="sxs-lookup"><span data-stu-id="2beb7-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="2beb7-112">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="2beb7-112">**\<configuration>**</span></span>](~/docs/framework/configure-apps/file-schema/configuration-element.md) | <span data-ttu-id="2beb7-113">通用語言執行平台和 .NET Framework 應用程式所使用之每個組態檔中的根項目。</span><span class="sxs-lookup"><span data-stu-id="2beb7-113">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="2beb7-114">子元素</span><span class="sxs-lookup"><span data-stu-id="2beb7-114">Child elements</span></span>

<span data-ttu-id="2beb7-115">無</span><span class="sxs-lookup"><span data-stu-id="2beb7-115">None</span></span>

## <a name="remarks"></a><span data-ttu-id="2beb7-116">備註</span><span class="sxs-lookup"><span data-stu-id="2beb7-116">Remarks</span></span>

<span data-ttu-id="2beb7-117">**\<SectionName >**項目是所定義的自訂項目[ **\<區段 >** ](~/docs/framework/configure-apps/file-schema/section-element.md)標記[ **\<c >** ](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md)項目。</span><span class="sxs-lookup"><span data-stu-id="2beb7-117">The **\<sectionName>** element is a custom element defined by a [**\<section>**](~/docs/framework/configure-apps/file-schema/section-element.md) tag in the [**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) element.</span></span> <span data-ttu-id="2beb7-118">組態系統會傳回<xref:System.Collections.IDictionary>物件時呼叫<xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="2beb7-118">The configuration system returns a <xref:System.Collections.IDictionary> object when you call <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="2beb7-119">範例</span><span class="sxs-lookup"><span data-stu-id="2beb7-119">Example</span></span>

<span data-ttu-id="2beb7-120">下列範例會宣告稱為自訂項目 **\<sampleSection >** ，其中包含所讀取的設定<xref:System.Configuration.SingleTagSectionHandler>類別：</span><span class="sxs-lookup"><span data-stu-id="2beb7-120">The following example declares a custom element called **\<sampleSection>** that contains settings read by the <xref:System.Configuration.SingleTagSectionHandler> class:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection" 
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="2beb7-121">組態檔</span><span class="sxs-lookup"><span data-stu-id="2beb7-121">Configuration file</span></span>

<span data-ttu-id="2beb7-122">此項目可以用於應用程式組態檔中，電腦組態檔 (*Machine.config*)，和*Web.config*不在應用程式目錄層級的檔案。</span><span class="sxs-lookup"><span data-stu-id="2beb7-122">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="2beb7-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="2beb7-123">See also</span></span>

[<span data-ttu-id="2beb7-124">適用於.NET Framework 組態檔結構描述</span><span class="sxs-lookup"><span data-stu-id="2beb7-124">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)