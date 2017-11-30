---
title: "ICLRRuntimeInfo 介面"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeInfo
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeInfo
helpviewer_keywords: ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 287e5ede-b3a7-4ef8-a756-4fca3f285a82
topic_type: apiref
caps.latest.revision: "27"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 86861ae1742cf520d1a5251c70a112b090ec429e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="iclrruntimeinfo-interface"></a><span data-ttu-id="9ec30-102">ICLRRuntimeInfo 介面</span><span class="sxs-lookup"><span data-stu-id="9ec30-102">ICLRRuntimeInfo Interface</span></span>
<span data-ttu-id="9ec30-103">提供方法，傳回特定 common language runtime (CLR) 的相關資訊包括版本、 目錄和負載狀態。</span><span class="sxs-lookup"><span data-stu-id="9ec30-103">Provides methods that return information about a specific common language runtime (CLR), including version, directory, and load status.</span></span> <span data-ttu-id="9ec30-104">此介面也提供執行階段特有的功能，但沒有初始化執行階段。</span><span class="sxs-lookup"><span data-stu-id="9ec30-104">This interface also provides runtime-specific functionality without initializing the runtime.</span></span> <span data-ttu-id="9ec30-105">其中包括執行階段相對[LoadLibrary](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md)方法中，執行階段模組專屬[GetProcAddress](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md)方法，並提供執行階段介面，透過[GetInterface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ec30-105">It includes the runtime-relative [LoadLibrary](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md) method, the runtime module-specific [GetProcAddress](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md) method, and runtime-provided interfaces through the [GetInterface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9ec30-106">方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-106">Methods</span></span>  
  
|<span data-ttu-id="9ec30-107">方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-107">Method</span></span>|<span data-ttu-id="9ec30-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ec30-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9ec30-109">BindAsLegacyV2Runtime 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-109">BindAsLegacyV2Runtime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md)|<span data-ttu-id="9ec30-110">將這個執行階段針對舊版 CLR 版本 2 的啟用原則決定所有的繫結。</span><span class="sxs-lookup"><span data-stu-id="9ec30-110">Binds this runtime for all legacy CLR version 2 activation policy decisions.</span></span>|  
|[<span data-ttu-id="9ec30-111">GetDefaultStartupFlags 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-111">GetDefaultStartupFlags Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getdefaultstartupflags-method.md)|<span data-ttu-id="9ec30-112">取得 CLR 啟動旗標和主機組態檔。</span><span class="sxs-lookup"><span data-stu-id="9ec30-112">Gets the CLR startup flags and host configuration file.</span></span>|  
|[<span data-ttu-id="9ec30-113">GetInterface 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-113">GetInterface Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)|<span data-ttu-id="9ec30-114">CLR 載入目前的處理序，並傳回執行階段介面指標，例如[ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)， [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)和[IMetaDataDispenser](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="9ec30-114">Loads the CLR into the current process and returns runtime interface pointers, such as [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md), [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md) and [IMetaDataDispenser](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md).</span></span> <span data-ttu-id="9ec30-115">這個方法會取代所有`CorBindTo*`函式。</span><span class="sxs-lookup"><span data-stu-id="9ec30-115">This method supersedes all the `CorBindTo*` functions.</span></span>|  
|[<span data-ttu-id="9ec30-116">GetProcAddress 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-116">GetProcAddress Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getprocaddress-method.md)|<span data-ttu-id="9ec30-117">取得指定的函式，此介面相關聯的 CLR 從匯出的位址。</span><span class="sxs-lookup"><span data-stu-id="9ec30-117">Gets the address of a specified function that was exported from the CLR associated with this interface.</span></span> <span data-ttu-id="9ec30-118">這個方法會取代[GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ec30-118">This method supersedes the [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) method.</span></span>|  
|[<span data-ttu-id="9ec30-119">GetRuntimeDirectory 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-119">GetRuntimeDirectory Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getruntimedirectory-method.md)|<span data-ttu-id="9ec30-120">取得此介面相關聯的 clr 安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="9ec30-120">Gets the installation directory of the CLR associated with this interface.</span></span> <span data-ttu-id="9ec30-121">這個方法會取代[GetCORSystemDirectory](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ec30-121">This method supersedes the [GetCORSystemDirectory](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md) method.</span></span>|  
|[<span data-ttu-id="9ec30-122">GetVersionString 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-122">GetVersionString Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getversionstring-method.md)|<span data-ttu-id="9ec30-123">取得 common language runtime (CLR) 版本資訊與相關給定[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)介面。</span><span class="sxs-lookup"><span data-stu-id="9ec30-123">Gets common language runtime (CLR) version information associated with a given [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span> <span data-ttu-id="9ec30-124">這個方法會取代[GetRequestedRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)和[GetRequestedRuntimeVersion](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ec30-124">This method supersedes the [GetRequestedRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md) and [GetRequestedRuntimeVersion](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md) methods.</span></span>|  
|[<span data-ttu-id="9ec30-125">IsLoadable 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-125">IsLoadable Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isloadable-method.md)|<span data-ttu-id="9ec30-126">表示此介面相關聯的執行階段是否可以載入目前的處理序不顧及其他執行階段，可能已經載入處理序。</span><span class="sxs-lookup"><span data-stu-id="9ec30-126">Indicates whether the runtime associated with this interface can be loaded into the current process, taking into account other runtimes that might already be loaded into the process.</span></span>|  
|[<span data-ttu-id="9ec30-127">IsLoaded 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-127">IsLoaded Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isloaded-method.md)|<span data-ttu-id="9ec30-128">指出是否在 CLR 與相關聯[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)介面載入處理序。</span><span class="sxs-lookup"><span data-stu-id="9ec30-128">Indicates whether the CLR associated with the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface is loaded into a process.</span></span>|  
|[<span data-ttu-id="9ec30-129">IsStarted 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-129">IsStarted Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-isstarted-method.md)|<span data-ttu-id="9ec30-130">指出是否在 CLR 與相關聯[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)介面已啟動。</span><span class="sxs-lookup"><span data-stu-id="9ec30-130">Indicates whether the CLR that is associated with the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface has been started.</span></span>|  
|[<span data-ttu-id="9ec30-131">LoadErrorString 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-131">LoadErrorString Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loaderrorstring-method.md)|<span data-ttu-id="9ec30-132">HRESULT 值轉譯為適當的錯誤訊息指定的文化特性。</span><span class="sxs-lookup"><span data-stu-id="9ec30-132">Translates an HRESULT value into an appropriate error message for the specified culture.</span></span> <span data-ttu-id="9ec30-133">這個方法會取代[LoadStringRC](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md)和[LoadStringRCEx](../../../../docs/framework/unmanaged-api/hosting/loadstringrcex-function.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ec30-133">This method supersedes the [LoadStringRC](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md) and [LoadStringRCEx](../../../../docs/framework/unmanaged-api/hosting/loadstringrcex-function.md) methods.</span></span>|  
|[<span data-ttu-id="9ec30-134">LoadLibrary 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-134">LoadLibrary Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-loadlibrary-method.md)|<span data-ttu-id="9ec30-135">從 CLR 所代表的 framework 目錄中載入文件庫[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)介面。</span><span class="sxs-lookup"><span data-stu-id="9ec30-135">Loads a library from the framework directory of the CLR represented by an [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span> <span data-ttu-id="9ec30-136">這個方法會取代[LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9ec30-136">This method supersedes the [LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md) method.</span></span>|  
|[<span data-ttu-id="9ec30-137">SetDefaultStartupFlags 方法</span><span class="sxs-lookup"><span data-stu-id="9ec30-137">SetDefaultStartupFlags Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-setdefaultstartupflags-method.md)|<span data-ttu-id="9ec30-138">設定 CLR 啟動旗標和主機組態檔。</span><span class="sxs-lookup"><span data-stu-id="9ec30-138">Sets the CLR startup flags and host configuration file.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9ec30-139">需求</span><span class="sxs-lookup"><span data-stu-id="9ec30-139">Requirements</span></span>  
 <span data-ttu-id="9ec30-140">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ec30-140">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ec30-141">**標頭：** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="9ec30-141">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="9ec30-142">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="9ec30-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9ec30-143">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ec30-143">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ec30-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ec30-144">See Also</span></span>  
 [<span data-ttu-id="9ec30-145">裝載介面</span><span class="sxs-lookup"><span data-stu-id="9ec30-145">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="9ec30-146">裝載</span><span class="sxs-lookup"><span data-stu-id="9ec30-146">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)