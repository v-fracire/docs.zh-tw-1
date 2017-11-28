---
title: "ICorDebugManagedCallback::BreakpointSetError 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback.BreakpointSetError
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback::BreakpointSetError
helpviewer_keywords:
- BreakpointSetError method [.NET Framework debugging]
- ICorDebugManagedCallback::BreakpointSetError method [.NET Framework debugging]
ms.assetid: f2b773a4-c4d0-429c-9717-51d6e2ed86af
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8d8d75261a0ac1211ec54252b698a2a1b17ccac2
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugmanagedcallbackbreakpointseterror-method"></a><span data-ttu-id="65717-102">ICorDebugManagedCallback::BreakpointSetError 方法</span><span class="sxs-lookup"><span data-stu-id="65717-102">ICorDebugManagedCallback::BreakpointSetError Method</span></span>
<span data-ttu-id="65717-103">Common language runtime 無法精確地繫結在 just-in-time (JIT) 編譯函式之前已設定的中斷點會告知偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="65717-103">Notifies the debugger that the common language runtime was unable to accurately bind a breakpoint that was set before a function was just-in-time (JIT) compiled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65717-104">語法</span><span class="sxs-lookup"><span data-stu-id="65717-104">Syntax</span></span>  
  
```  
HRESULT BreakpointSetError (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugBreakpoint *pBreakpoint,  
    [in] DWORD                dwError  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="65717-105">參數</span><span class="sxs-lookup"><span data-stu-id="65717-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="65717-106">[in]代表應用程式定義域，其中包含未繫結的中斷點 ICorDebugAppDomain 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="65717-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the unbound breakpoint.</span></span>  
  
 `pThread`  
 <span data-ttu-id="65717-107">[in]表示包含繫結的中斷點的執行緒 ICorDebugThread 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="65717-107">[in] A pointer to an ICorDebugThread object that represents the thread that contains the unbound breakpoint.</span></span>  
  
 `pBreakpoint`  
 <span data-ttu-id="65717-108">[in]ICorDebugBreakpoint 物件，表示未繫結的中斷點指標。</span><span class="sxs-lookup"><span data-stu-id="65717-108">[in] A pointer to an ICorDebugBreakpoint object that represents the unbound breakpoint.</span></span>  
  
 `dwError`  
 <span data-ttu-id="65717-109">[in]整數，表示的錯誤。</span><span class="sxs-lookup"><span data-stu-id="65717-109">[in] An integer that indicates the error.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="65717-110">備註</span><span class="sxs-lookup"><span data-stu-id="65717-110">Remarks</span></span>  
 <span data-ttu-id="65717-111">永遠不會叫用指定的中斷點。</span><span class="sxs-lookup"><span data-stu-id="65717-111">The given breakpoint will never be hit.</span></span> <span data-ttu-id="65717-112">偵錯工具應該停用，並將它重新繫結。</span><span class="sxs-lookup"><span data-stu-id="65717-112">The debugger should deactivate and rebind it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65717-113">需求</span><span class="sxs-lookup"><span data-stu-id="65717-113">Requirements</span></span>  
 <span data-ttu-id="65717-114">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="65717-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="65717-115">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="65717-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="65717-116">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="65717-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="65717-117">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="65717-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65717-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65717-118">See Also</span></span>  
 [<span data-ttu-id="65717-119">ICorDebugManagedCallback 介面</span><span class="sxs-lookup"><span data-stu-id="65717-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)