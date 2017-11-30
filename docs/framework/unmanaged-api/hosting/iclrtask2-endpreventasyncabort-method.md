---
title: "ICLRTask2::EndPreventAsyncAbort 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRTask2.EndPreventAsyncAbort
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRTask2::EndPreventAsyncAbort
helpviewer_keywords:
- EndPreventAsyncAbort method [.NET Framework hosting]
- ICLRTask2::EndPreventAsyncAbort method [.NET Framework hosting]
ms.assetid: d8013659-e3df-44b3-814f-a6b534ce62f8
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c76a75004b4593e8e93aa4dd999c85c0fb7cf38a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="iclrtask2endpreventasyncabort-method"></a><span data-ttu-id="408ca-102">ICLRTask2::EndPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="408ca-102">ICLRTask2::EndPreventAsyncAbort Method</span></span>
<span data-ttu-id="408ca-103">可讓新的或暫止的執行緒中止要求，以產生的執行緒會中止目前的執行緒上。</span><span class="sxs-lookup"><span data-stu-id="408ca-103">Allows new or pending thread abort requests to result in thread aborts on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="408ca-104">語法</span><span class="sxs-lookup"><span data-stu-id="408ca-104">Syntax</span></span>  
  
```  
HRESULT EndPreventAsyncAbort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="408ca-105">傳回值</span><span class="sxs-lookup"><span data-stu-id="408ca-105">Return Value</span></span>  
 <span data-ttu-id="408ca-106">這個方法會傳回下列特定的 HRESULT 以及 HRESULT 錯誤，以指出方法失敗。</span><span class="sxs-lookup"><span data-stu-id="408ca-106">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="408ca-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="408ca-107">HRESULT</span></span>|<span data-ttu-id="408ca-108">描述</span><span class="sxs-lookup"><span data-stu-id="408ca-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="408ca-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="408ca-109">S_OK</span></span>|<span data-ttu-id="408ca-110">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="408ca-110">The method completed successfully.</span></span>|  
|<span data-ttu-id="408ca-111">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="408ca-111">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="408ca-112">這不是目前執行緒的執行緒上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="408ca-112">The method was called on a thread which is not the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="408ca-113">備註</span><span class="sxs-lookup"><span data-stu-id="408ca-113">Remarks</span></span>  
 <span data-ttu-id="408ca-114">目前的執行緒呼叫這個方法會在延遲執行緒中止計數器以一。</span><span class="sxs-lookup"><span data-stu-id="408ca-114">Calling this method decrements the delay-thread-abort counter for the current thread by one.</span></span>  
  
 <span data-ttu-id="408ca-115">呼叫[iclrtask2:: Beginpreventasyncabort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)和`EndPreventAsyncAbort`可以巢狀。</span><span class="sxs-lookup"><span data-stu-id="408ca-115">Calls to [ICLRTask2::BeginPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md) and `EndPreventAsyncAbort` can be nested.</span></span> <span data-ttu-id="408ca-116">只要計數器是小於或等於零，執行緒中止目前的執行緒會延遲。</span><span class="sxs-lookup"><span data-stu-id="408ca-116">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span>  
  
 <span data-ttu-id="408ca-117">這項功能所公開的功能是由虛擬機器 (VM) 內部使用。</span><span class="sxs-lookup"><span data-stu-id="408ca-117">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="408ca-118">不當使用這些方法可能導致 VM 未指定的行為。</span><span class="sxs-lookup"><span data-stu-id="408ca-118">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="408ca-119">例如，呼叫`EndPreventAsyncAbort`情況下先呼叫`BeginPreventAsyncAbort`VM 之前會遞增它時，無法設定計數器為零。</span><span class="sxs-lookup"><span data-stu-id="408ca-119">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="408ca-120">同樣地，內部計數器不會檢查溢位。</span><span class="sxs-lookup"><span data-stu-id="408ca-120">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="408ca-121">如果它超過其整數類資料的限制，因為主機和 VM，就會遞增，結果行為是未指定。</span><span class="sxs-lookup"><span data-stu-id="408ca-121">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="408ca-122">需求</span><span class="sxs-lookup"><span data-stu-id="408ca-122">Requirements</span></span>  
 <span data-ttu-id="408ca-123">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="408ca-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="408ca-124">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="408ca-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="408ca-125">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="408ca-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="408ca-126">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="408ca-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="408ca-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="408ca-127">See Also</span></span>  
 [<span data-ttu-id="408ca-128">BeginPreventAsyncAbort 方法</span><span class="sxs-lookup"><span data-stu-id="408ca-128">BeginPreventAsyncAbort Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)  
 [<span data-ttu-id="408ca-129">ICLRTask2 介面</span><span class="sxs-lookup"><span data-stu-id="408ca-129">ICLRTask2 Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-interface.md)  
 [<span data-ttu-id="408ca-130">ICLRTaskManager 介面</span><span class="sxs-lookup"><span data-stu-id="408ca-130">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="408ca-131">IHostTask 介面</span><span class="sxs-lookup"><span data-stu-id="408ca-131">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="408ca-132">IHostTaskManager 介面</span><span class="sxs-lookup"><span data-stu-id="408ca-132">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [<span data-ttu-id="408ca-133">裝載介面</span><span class="sxs-lookup"><span data-stu-id="408ca-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)