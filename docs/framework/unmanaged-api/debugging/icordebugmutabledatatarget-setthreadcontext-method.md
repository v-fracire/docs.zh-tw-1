---
title: "ICorDebugMutableDataTarget::SetThreadContext 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 8c0d01d5-67e5-4522-9ccf-c8f3a78cb4fd
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8c43ef5405ed582cc55af69d7f41887c0615965f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmutabledatatargetsetthreadcontext-method"></a><span data-ttu-id="5f1e0-102">ICorDebugMutableDataTarget::SetThreadContext 方法</span><span class="sxs-lookup"><span data-stu-id="5f1e0-102">ICorDebugMutableDataTarget::SetThreadContext Method</span></span>
<span data-ttu-id="5f1e0-103">設定執行緒的內容 (登錄值)。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-103">Sets the context (register values) for a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f1e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="5f1e0-104">Syntax</span></span>  
  
```  
HRESULT SetThreadContext(  
   [in] DWORD dwThreadID,  
   [in] ULONG32 contextSize,   [in, size_is(contextSize)] const BYTE * pContext);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5f1e0-105">參數</span><span class="sxs-lookup"><span data-stu-id="5f1e0-105">Parameters</span></span>  
 `dwThreadID`  
 <span data-ttu-id="5f1e0-106">[in] 作業系統定義的執行緒識別項。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-106">[in] The operating system-defined thread identifier.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="5f1e0-107">[in] 所要寫入的 `pContext` 緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-107">[in] The size of the `pContext` buffer to be written.</span></span>  
  
 `pContext`  
 <span data-ttu-id="5f1e0-108">[in] 所要寫入的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-108">[in] A pointer to the bytes to be written.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5f1e0-109">備註</span><span class="sxs-lookup"><span data-stu-id="5f1e0-109">Remarks</span></span>  
 <span data-ttu-id="5f1e0-110">`SetThreadContext` 方法會針對作業系統定義之 `dwThreadID` 引數所指定的執行緒，更新目前的內容。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-110">The `SetThreadContext` method updates the current context for the thread specified by the operating system-defined `dwThreadID` argument.</span></span> <span data-ttu-id="5f1e0-111">內容記錄的格式取決於所指定的平台[icordebugdatatarget:: Getplatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-111">The format of the context record is determined by the platform indicated by the [ICorDebugDataTarget::GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) method.</span></span> <span data-ttu-id="5f1e0-112">在 Windows 中，這是[內容](http://msdn.microsoft.com/library/windows/desktop/ms679284.aspx)結構。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-112">On Windows, this is a [CONTEXT](http://msdn.microsoft.com/library/windows/desktop/ms679284.aspx) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f1e0-113">需求</span><span class="sxs-lookup"><span data-stu-id="5f1e0-113">Requirements</span></span>  
 <span data-ttu-id="5f1e0-114">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f1e0-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f1e0-115">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5f1e0-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5f1e0-116">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5f1e0-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5f1e0-117">**.NET framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f1e0-117">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f1e0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f1e0-118">See Also</span></span>  
 [<span data-ttu-id="5f1e0-119">ICorDebugMutableDataTarget 介面</span><span class="sxs-lookup"><span data-stu-id="5f1e0-119">ICorDebugMutableDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)  
 [<span data-ttu-id="5f1e0-120">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="5f1e0-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)