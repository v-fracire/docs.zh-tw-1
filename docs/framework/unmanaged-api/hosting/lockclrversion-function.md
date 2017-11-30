---
title: "LockClrVersion 函式"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: LockClrVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type: DLLExport
f1_keywords: LockClrVersion
helpviewer_keywords: LockClrVersion function [.NET Framework hosting]
ms.assetid: 1318ee37-c43b-40eb-bbe8-88fc46453d74
topic_type: apiref
caps.latest.revision: "15"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: be41ae47f78a41e2f2be10a1e38d938dde9a4701
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="lockclrversion-function"></a><span data-ttu-id="d25a5-102">LockClrVersion 函式</span><span class="sxs-lookup"><span data-stu-id="d25a5-102">LockClrVersion Function</span></span>
<span data-ttu-id="d25a5-103">可讓主機判斷處理序中先明確初始化 CLR 使用的 common language runtime (CLR) 版本。</span><span class="sxs-lookup"><span data-stu-id="d25a5-103">Allows the host to determine which version of the common language runtime (CLR) will be used within the process before explicitly initializing the CLR.</span></span>  
  
 <span data-ttu-id="d25a5-104">此函式中已被取代[!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]。</span><span class="sxs-lookup"><span data-stu-id="d25a5-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d25a5-105">語法</span><span class="sxs-lookup"><span data-stu-id="d25a5-105">Syntax</span></span>  
  
```  
HRESULT LockClrVersion (  
    [in] FLockClrVersionCallback   hostCallback,  
    [in] FLockClrVersionCallback  *pBeginHostSetup,  
    [in] FLockClrVersionCallback  *pEndHostSetup  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d25a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="d25a5-106">Parameters</span></span>  
 `hostCallback`  
 <span data-ttu-id="d25a5-107">[in]要由 CLR 在初始化時呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="d25a5-107">[in] The function to be called by the CLR upon initialization.</span></span>  
  
 `pBeginHostSetup`  
 <span data-ttu-id="d25a5-108">[in]正在啟動初始設定主應用程式通知 CLR 所要呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="d25a5-108">[in] The function to be called by the host to inform the CLR that initialization is starting.</span></span>  
  
 `pEndHostSetup`  
 <span data-ttu-id="d25a5-109">[in]函式由主機呼叫，通知 CLR 初始化已完成。</span><span class="sxs-lookup"><span data-stu-id="d25a5-109">[in] The function to be called by the host to inform the CLR that initialization is complete.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d25a5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d25a5-110">Return Value</span></span>  
 <span data-ttu-id="d25a5-111">這個方法會傳回標準的 COM 錯誤代碼，除了下列的值定義了 WinError.h 中。</span><span class="sxs-lookup"><span data-stu-id="d25a5-111">This method returns standard COM error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="d25a5-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d25a5-112">Return code</span></span>|<span data-ttu-id="d25a5-113">描述</span><span class="sxs-lookup"><span data-stu-id="d25a5-113">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="d25a5-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d25a5-114">S_OK</span></span>|<span data-ttu-id="d25a5-115">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="d25a5-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="d25a5-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d25a5-116">E_INVALIDARG</span></span>|<span data-ttu-id="d25a5-117">一或多個引數為 null。</span><span class="sxs-lookup"><span data-stu-id="d25a5-117">One or more of the arguments is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d25a5-118">備註</span><span class="sxs-lookup"><span data-stu-id="d25a5-118">Remarks</span></span>  
 <span data-ttu-id="d25a5-119">主機會呼叫`LockClrVersion`之前初始化 CLR。</span><span class="sxs-lookup"><span data-stu-id="d25a5-119">The host calls `LockClrVersion` before initializing the CLR.</span></span> <span data-ttu-id="d25a5-120">`LockClrVersion`接受三個參數，都是類型的回呼[FLockClrVersionCallback](../../../../docs/framework/unmanaged-api/hosting/flockclrversioncallback-function-pointer.md)。</span><span class="sxs-lookup"><span data-stu-id="d25a5-120">`LockClrVersion` takes three parameters, all of which are callbacks of type [FLockClrVersionCallback](../../../../docs/framework/unmanaged-api/hosting/flockclrversioncallback-function-pointer.md).</span></span> <span data-ttu-id="d25a5-121">此類型定義，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d25a5-121">This type is defined as follows.</span></span>  
  
```  
typedef HRESULT ( __stdcall *FLockClrVersionCallback ) ();  
```  
  
 <span data-ttu-id="d25a5-122">在執行階段初始化時，執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d25a5-122">The following steps occur upon initialization of the runtime:</span></span>  
  
1.  <span data-ttu-id="d25a5-123">主機會呼叫[CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)或其他執行階段初始化函式的其中一個。</span><span class="sxs-lookup"><span data-stu-id="d25a5-123">The host calls [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) or one of the other runtime initialization functions.</span></span> <span data-ttu-id="d25a5-124">或者，主應用程式無法初始化執行階段使用 COM 物件啟動。</span><span class="sxs-lookup"><span data-stu-id="d25a5-124">Alternatively, the host could initialize the runtime using COM object activation.</span></span>  
  
2.  <span data-ttu-id="d25a5-125">執行階段呼叫的函式所指定`hostCallback`參數。</span><span class="sxs-lookup"><span data-stu-id="d25a5-125">The runtime calls the function specified by the `hostCallback` parameter.</span></span>  
  
3.  <span data-ttu-id="d25a5-126">所指定的函數`hostCallback`使下列呼叫順序：</span><span class="sxs-lookup"><span data-stu-id="d25a5-126">The function specified by `hostCallback` then makes the following sequence of calls:</span></span>  
  
    -   <span data-ttu-id="d25a5-127">所指定的函數`pBeginHostSetup`參數。</span><span class="sxs-lookup"><span data-stu-id="d25a5-127">The function specified by the `pBeginHostSetup` parameter.</span></span>  
  
    -   <span data-ttu-id="d25a5-128">`CorBindToRuntimeEx`（或另一個執行階段初始化函式）。</span><span class="sxs-lookup"><span data-stu-id="d25a5-128">`CorBindToRuntimeEx` (or another runtime initialization function).</span></span>  
  
    -   <span data-ttu-id="d25a5-129">[Iclrruntimehost:: Sethostcontrol](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-sethostcontrol-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d25a5-129">[ICLRRuntimeHost::SetHostControl](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-sethostcontrol-method.md).</span></span>  
  
    -   <span data-ttu-id="d25a5-130">[Iclrruntimehost:: Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d25a5-130">[ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md).</span></span>  
  
    -   <span data-ttu-id="d25a5-131">所指定的函數`pEndHostSetup`參數。</span><span class="sxs-lookup"><span data-stu-id="d25a5-131">The function specified by the `pEndHostSetup` parameter.</span></span>  
  
 <span data-ttu-id="d25a5-132">從所有的呼叫`pBeginHostSetup`至`pEndHostSetup`必須發生在單一執行緒或 fiber，具有相同的邏輯堆疊。</span><span class="sxs-lookup"><span data-stu-id="d25a5-132">All the calls from `pBeginHostSetup` to `pEndHostSetup` must occur on a single thread or fiber, with the same logical stack.</span></span> <span data-ttu-id="d25a5-133">這個執行緒可以不同的執行緒`hostCallback`呼叫。</span><span class="sxs-lookup"><span data-stu-id="d25a5-133">This thread can be different from the thread upon which `hostCallback` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d25a5-134">需求</span><span class="sxs-lookup"><span data-stu-id="d25a5-134">Requirements</span></span>  
 <span data-ttu-id="d25a5-135">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d25a5-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d25a5-136">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d25a5-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d25a5-137">**程式庫：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d25a5-137">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d25a5-138">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d25a5-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d25a5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d25a5-139">See Also</span></span>  
 [<span data-ttu-id="d25a5-140">已被取代的 CLR 裝載函式</span><span class="sxs-lookup"><span data-stu-id="d25a5-140">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)