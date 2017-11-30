---
title: "IAppDomainSetup 介面"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAppDomainSetup
api_location: mscoree.dll
api_type: COM
f1_keywords: IAppDomainSetup
helpviewer_keywords: IAppDomainSetup interface [.NET Framework hosting]
ms.assetid: 1844da85-c031-40bf-bea4-1a3d12a36c8c
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e6ed5ea00799fff70626114257efef2d06b505ae
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="iappdomainsetup-interface"></a><span data-ttu-id="132c8-102">IAppDomainSetup 介面</span><span class="sxs-lookup"><span data-stu-id="132c8-102">IAppDomainSetup Interface</span></span>
<span data-ttu-id="132c8-103">提供可讓主應用程式設定的屬性<xref:System.AppDomain?displayProperty=nameWithType>型別之前呼叫[icorruntimehost:: Createdomainex](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md)方法來建立它。</span><span class="sxs-lookup"><span data-stu-id="132c8-103">Provides properties that allow the host to configure an <xref:System.AppDomain?displayProperty=nameWithType> type before calling the [ICorRuntimeHost::CreateDomainEx](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-createdomainex-method.md) method to create it.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="132c8-104">屬性</span><span class="sxs-lookup"><span data-stu-id="132c8-104">Properties</span></span>  
  
|<span data-ttu-id="132c8-105">屬性</span><span class="sxs-lookup"><span data-stu-id="132c8-105">Property</span></span>|<span data-ttu-id="132c8-106">說明</span><span class="sxs-lookup"><span data-stu-id="132c8-106">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.AppDomainSetup.ApplicationBase%2A>|<span data-ttu-id="132c8-107">取得或設定包含應用程式的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="132c8-107">Gets or sets the name of the directory that contains the application.</span></span>|  
|<xref:System.AppDomainSetup.ApplicationName%2A>|<span data-ttu-id="132c8-108">取得或設定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="132c8-108">Gets or sets the name of the application.</span></span>|  
|<xref:System.AppDomainSetup.CachePath%2A>|<span data-ttu-id="132c8-109">取得或設定檔案已陰影複製的應用程式特定區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="132c8-109">Gets or sets the name of an area specific to the application where files are shadow-copied.</span></span>|  
|<xref:System.AppDomainSetup.ConfigurationFile%2A>|<span data-ttu-id="132c8-110">取得或設定應用程式的組態檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="132c8-110">Gets or sets the name of the configuration file for an application.</span></span>|  
|<xref:System.AppDomainSetup.DynamicBase%2A>|<span data-ttu-id="132c8-111">取得或設定儲存及存取動態產生的檔案的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="132c8-111">Gets or sets the name of the directory where dynamically generated files are stored and accessed.</span></span>|  
|<xref:System.AppDomainSetup.LicenseFile%2A>|<span data-ttu-id="132c8-112">取得或設定與這個定義域相關聯的使用權檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="132c8-112">Gets or sets the path to the license file that is associated with this domain.</span></span>|  
|<xref:System.AppDomainSetup.PrivateBinPath%2A>|<span data-ttu-id="132c8-113">取得或設定與結合的目錄清單<xref:System.AppDomainSetup.ApplicationBase%2A>探查私用組件的目錄。</span><span class="sxs-lookup"><span data-stu-id="132c8-113">Gets or sets the list of directories combined with the <xref:System.AppDomainSetup.ApplicationBase%2A> directory to probe for private assemblies.</span></span>|  
|<xref:System.AppDomainSetup.PrivateBinPathProbe%2A>|<span data-ttu-id="132c8-114">取得或設定字串值包含或排除<xref:System.AppDomainSetup.ApplicationBase%2A>應用程式的搜尋路徑中。</span><span class="sxs-lookup"><span data-stu-id="132c8-114">Gets or sets a string value that includes or excludes <xref:System.AppDomainSetup.ApplicationBase%2A> from the search path for the application.</span></span>|  
|<xref:System.AppDomainSetup.ShadowCopyDirectories%2A>|<span data-ttu-id="132c8-115">取得或設定包含要陰影複製組件的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="132c8-115">Gets or sets the names of the directories that contain assemblies to be shadow-copied.</span></span>|  
|<xref:System.AppDomainSetup.ShadowCopyFiles%2A>|<span data-ttu-id="132c8-116">取得或設定指示陰影複製開啟或關閉的字串。</span><span class="sxs-lookup"><span data-stu-id="132c8-116">Gets or sets a string that indicates whether shadow-copying is turned on or off.</span></span> <span data-ttu-id="132c8-117">有效值為"true"或"false"。</span><span class="sxs-lookup"><span data-stu-id="132c8-117">Valid values are "true" or "false".</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="132c8-118">備註</span><span class="sxs-lookup"><span data-stu-id="132c8-118">Remarks</span></span>  
 <span data-ttu-id="132c8-119">`IAppDomainSetup`介面對應至 managed<xref:System.IAppDomainSetup>介面，其中<xref:System.AppDomainSetup>型別會實作。</span><span class="sxs-lookup"><span data-stu-id="132c8-119">The `IAppDomainSetup` interface corresponds to the managed <xref:System.IAppDomainSetup> interface, which the <xref:System.AppDomainSetup> type implements.</span></span> <span data-ttu-id="132c8-120">請參閱<xref:System.IAppDomainSetup?displayProperty=nameWithType>如其屬性的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="132c8-120">See <xref:System.IAppDomainSetup?displayProperty=nameWithType> for detailed descriptions of its properties.</span></span>  
  
 <span data-ttu-id="132c8-121">`IAppDomainSetup`表示可以加入的組件繫結資訊<xref:System.AppDomain>之前建立的執行個體。</span><span class="sxs-lookup"><span data-stu-id="132c8-121">`IAppDomainSetup` represents assembly binding information that can be added to an <xref:System.AppDomain> instance before its creation.</span></span> <span data-ttu-id="132c8-122">例如，主機可以設定<xref:System.AppDomainSetup.ApplicationBase%2A>屬性，以建立根目錄，探查 common language runtime (CLR) managed 組件。</span><span class="sxs-lookup"><span data-stu-id="132c8-122">For example, a host can set the <xref:System.AppDomainSetup.ApplicationBase%2A> property to establish a root directory, which the common language runtime (CLR) probes for managed assemblies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="132c8-123">需求</span><span class="sxs-lookup"><span data-stu-id="132c8-123">Requirements</span></span>  
 <span data-ttu-id="132c8-124">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="132c8-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="132c8-125">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="132c8-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="132c8-126">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="132c8-126">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="132c8-127">**.NET framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="132c8-127">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="132c8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="132c8-128">See Also</span></span>  
 <xref:System.AppDomain>  
 <xref:System.AppDomainSetup>  
 <xref:System.IAppDomainSetup>  
 [<span data-ttu-id="132c8-129">裝載介面</span><span class="sxs-lookup"><span data-stu-id="132c8-129">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)