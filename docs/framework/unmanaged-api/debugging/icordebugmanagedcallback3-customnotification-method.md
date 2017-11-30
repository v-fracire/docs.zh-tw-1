---
title: "ICorDebugManagedCallback3::CustomNotification 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback3.CustomNotification Method
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback3::CustomNotification
helpviewer_keywords:
- ICorDebugManagedCallback3::CustomNotification method [.NET Framework debugging]
- CustomNotification method [.NET Framework debugging]
ms.assetid: 5e5422ac-afa1-403d-a894-2d7348673e38
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: edff9c4b19131fcdfd4510c4020612acb43b6305
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmanagedcallback3customnotification-method"></a><span data-ttu-id="fc27d-102">ICorDebugManagedCallback3::CustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="fc27d-102">ICorDebugManagedCallback3::CustomNotification Method</span></span>
<span data-ttu-id="fc27d-103">表示已發出的自訂偵錯工具通知。</span><span class="sxs-lookup"><span data-stu-id="fc27d-103">Indicates that a custom debugger notification has been raised.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fc27d-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc27d-104">Syntax</span></span>  
  
```  
HRESULT CustomNotification(ICorDebugThread *    pThread,  
                           ICorDebugAppDomain * pAppDomain);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fc27d-105">參數</span><span class="sxs-lookup"><span data-stu-id="fc27d-105">Parameters</span></span>  
 `pThread`  
 <span data-ttu-id="fc27d-106">[in]引發通知之執行緒的指標。</span><span class="sxs-lookup"><span data-stu-id="fc27d-106">[in] A pointer to the thread that raised the notification.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="fc27d-107">[in]包含引發通知的執行緒的應用程式定義域的指標。</span><span class="sxs-lookup"><span data-stu-id="fc27d-107">[in] A pointer to the application domain that contains the thread that raised the notification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fc27d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc27d-108">Return Value</span></span>  
 <span data-ttu-id="fc27d-109">這個方法會傳回下列特定的 HRESULT 以及 HRESULT 錯誤，以指出方法失敗。</span><span class="sxs-lookup"><span data-stu-id="fc27d-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="fc27d-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="fc27d-110">HRESULT</span></span>|<span data-ttu-id="fc27d-111">描述</span><span class="sxs-lookup"><span data-stu-id="fc27d-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="fc27d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc27d-112">S_OK</span></span>|<span data-ttu-id="fc27d-113">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="fc27d-113">The method completed successfully.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="fc27d-114">例外狀況</span><span class="sxs-lookup"><span data-stu-id="fc27d-114">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fc27d-115">備註</span><span class="sxs-lookup"><span data-stu-id="fc27d-115">Remarks</span></span>  
 <span data-ttu-id="fc27d-116">後續呼叫[icordebugthread4:: Getcurrentcustomdebuggernotification](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getcurrentcustomdebuggernotification-method.md)方法會擷取已傳遞給執行緒物件<xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType>方法。</span><span class="sxs-lookup"><span data-stu-id="fc27d-116">A subsequent call to the [ICorDebugThread4::GetCurrentCustomDebuggerNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getcurrentcustomdebuggernotification-method.md) method retrieves the thread object that was passed to the <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="fc27d-117">執行緒物件的型別必須先前已啟用藉由呼叫[icordebugprocess3:: Setenablecustomnotification](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-setenablecustomnotification-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="fc27d-117">The thread object's type must have been previously enabled by calling the [ICorDebugProcess3::SetEnableCustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-setenablecustomnotification-method.md) method.</span></span> <span data-ttu-id="fc27d-118">偵錯工具可以讀取特定類型的參數，執行緒物件的欄位，而且回應儲存到欄位。</span><span class="sxs-lookup"><span data-stu-id="fc27d-118">The debugger can read type-specific parameters from the fields of the thread object, and can store responses into fields.</span></span>  
  
 <span data-ttu-id="fc27d-119">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)介面會加諸的任何原則類型的通知或其內容，以及通知的語意都完全偵錯工具、 應用程式和.NET Framework 之間的合約。</span><span class="sxs-lookup"><span data-stu-id="fc27d-119">The [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface imposes no policy on the types of notifications or their contents, and the semantics of the notifications are strictly a contract between debuggers, applications, and the .NET Framework.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fc27d-120">需求</span><span class="sxs-lookup"><span data-stu-id="fc27d-120">Requirements</span></span>  
 <span data-ttu-id="fc27d-121">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fc27d-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc27d-122">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fc27d-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fc27d-123">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fc27d-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fc27d-124">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fc27d-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc27d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc27d-125">See Also</span></span>  
 [<span data-ttu-id="fc27d-126">ICorDebugManagedCallback3 介面</span><span class="sxs-lookup"><span data-stu-id="fc27d-126">ICorDebugManagedCallback3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-interface.md)  
 [<span data-ttu-id="fc27d-127">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="fc27d-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="fc27d-128">偵錯</span><span class="sxs-lookup"><span data-stu-id="fc27d-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)