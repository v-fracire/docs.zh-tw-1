---
title: "ICorDebugMDA 介面"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugMDA
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugMDA
helpviewer_keywords: ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 8ecbb854-295c-4dd4-b9fc-01ebeac46e06
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 00a003ee060de59fe0eb8ce8f740a620d77a7c85
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmda-interface"></a><span data-ttu-id="08804-102">ICorDebugMDA 介面</span><span class="sxs-lookup"><span data-stu-id="08804-102">ICorDebugMDA Interface</span></span>
<span data-ttu-id="08804-103">表示 Managed 偵錯助理 (MDA) 訊息。</span><span class="sxs-lookup"><span data-stu-id="08804-103">Represents a managed debugging assistant (MDA) message.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="08804-104">方法</span><span class="sxs-lookup"><span data-stu-id="08804-104">Methods</span></span>  
  
|<span data-ttu-id="08804-105">方法</span><span class="sxs-lookup"><span data-stu-id="08804-105">Method</span></span>|<span data-ttu-id="08804-106">說明</span><span class="sxs-lookup"><span data-stu-id="08804-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="08804-107">GetDescription 方法</span><span class="sxs-lookup"><span data-stu-id="08804-107">GetDescription Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getdescription-method.md)|<span data-ttu-id="08804-108">取得字串，包含這個 MDA 的描述。</span><span class="sxs-lookup"><span data-stu-id="08804-108">Gets a string containing a description of this MDA.</span></span>|  
|[<span data-ttu-id="08804-109">GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="08804-109">GetFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getflags-method.md)|<span data-ttu-id="08804-110">取得與這個 MDA 相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="08804-110">Gets the flags associated with this MDA.</span></span>|  
|[<span data-ttu-id="08804-111">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="08804-111">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getname-method.md)|<span data-ttu-id="08804-112">取得字串，包含這個 MDA 的名稱。</span><span class="sxs-lookup"><span data-stu-id="08804-112">Gets a string containing the name of this MDA.</span></span>|  
|[<span data-ttu-id="08804-113">GetOSThreadId 方法</span><span class="sxs-lookup"><span data-stu-id="08804-113">GetOSThreadId Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getosthreadid-method.md)|<span data-ttu-id="08804-114">取得這個 MDA 賴以執行的作業系統執行緒識別項。</span><span class="sxs-lookup"><span data-stu-id="08804-114">Gets the operating system thread identifier upon which this MDA is executing.</span></span>|  
|[<span data-ttu-id="08804-115">GetXML 方法</span><span class="sxs-lookup"><span data-stu-id="08804-115">GetXML Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getxml-method.md)|<span data-ttu-id="08804-116">取得完整這個 MDA 相關聯的 XML 資料流。</span><span class="sxs-lookup"><span data-stu-id="08804-116">Gets the full XML stream associated with this MDA.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08804-117">備註</span><span class="sxs-lookup"><span data-stu-id="08804-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="08804-118">這個介面不支援跨電腦或跨處理序的遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="08804-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08804-119">需求</span><span class="sxs-lookup"><span data-stu-id="08804-119">Requirements</span></span>  
 <span data-ttu-id="08804-120">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="08804-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08804-121">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="08804-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="08804-122">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08804-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08804-123">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08804-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08804-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08804-124">See Also</span></span>  
 [<span data-ttu-id="08804-125">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="08804-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="08804-126">使用 Managed 偵錯助理診斷錯誤</span><span class="sxs-lookup"><span data-stu-id="08804-126">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)