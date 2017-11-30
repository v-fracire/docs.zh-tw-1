---
title: "ICorProfilerCallback5 介面"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback5
api_location: Mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback5
helpviewer_keywords: ICorProfilerCallback5 interface [.NET Framework profiling]
ms.assetid: 61d2e9ef-5f1f-4771-8847-239616e35d84
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 1a862707dc64efbf3a9b1604a0e6a4ff1be81b43
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback5-interface"></a><span data-ttu-id="e8588-102">ICorProfilerCallback5 介面</span><span class="sxs-lookup"><span data-stu-id="e8588-102">ICorProfilerCallback5 Interface</span></span>
<span data-ttu-id="e8588-103">補充資訊可協助分析工具搭配使用時，識別即時物件的完整結束[icorprofilercallback:: Rootreferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md)或[icorprofilercallback2:: Rootreferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md)方法並搭配[icorprofilercallback:: Objectreferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md)和[ConditionalWeakTableElementReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-conditionalweaktableelementreferences-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="e8588-103">Supplements information to help a profiler identify the full closure of live objects, when used with either the [ICorProfilerCallback::RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) or [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) method together with the [ICorProfilerCallback::ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md) and [ConditionalWeakTableElementReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-conditionalweaktableelementreferences-method.md) methods.</span></span>  
  
 <span data-ttu-id="e8588-104">`ICorProfilerCallback5` 必須由 Managed 記憶體分析工具實作，以訂閱與相依性控制代碼相關的通知。</span><span class="sxs-lookup"><span data-stu-id="e8588-104">`ICorProfilerCallback5` must be implemented by a managed memory profiler to subscribe to notifications related to dependent handles.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e8588-105">備註</span><span class="sxs-lookup"><span data-stu-id="e8588-105">Remarks</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e8588-106">方法</span><span class="sxs-lookup"><span data-stu-id="e8588-106">Methods</span></span>  
  
|<span data-ttu-id="e8588-107">方法</span><span class="sxs-lookup"><span data-stu-id="e8588-107">Method</span></span>|<span data-ttu-id="e8588-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8588-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e8588-109">ConditionalWeakTableElementReferences 方法</span><span class="sxs-lookup"><span data-stu-id="e8588-109">ConditionalWeakTableElementReferences Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-conditionalweaktableelementreferences-method.md)|<span data-ttu-id="e8588-110">識別那些根目錄透過直接成員欄位參考以及透過 `ConditionalWeakTable` 相依性來參考之物件的可轉移結束。</span><span class="sxs-lookup"><span data-stu-id="e8588-110">Identifies the transitive closure of objects referenced by those roots through both direct member field references and through `ConditionalWeakTable` dependencies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e8588-111">需求</span><span class="sxs-lookup"><span data-stu-id="e8588-111">Requirements</span></span>  
 <span data-ttu-id="e8588-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8588-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8588-113">**標頭：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e8588-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e8588-114">**.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8588-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8588-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8588-115">See Also</span></span>  
 [<span data-ttu-id="e8588-116">分析介面</span><span class="sxs-lookup"><span data-stu-id="e8588-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="e8588-117">ICorProfilerCallback2 介面</span><span class="sxs-lookup"><span data-stu-id="e8588-117">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)