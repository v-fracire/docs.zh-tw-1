---
title: "ICorDebugBreakpoint::Activate 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugBreakpoint.Activate
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugBreakpoint::Activate
helpviewer_keywords:
- ICorDebugBreakpoint::Activate method [.NET Framework debugging]
- Activate method [.NET Framework debugging]
ms.assetid: e30c29f7-3f19-4081-b572-a731aa14cd44
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7112ff7d18d0232da42013dfd533689cb8c5f0ab
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugbreakpointactivate-method"></a><span data-ttu-id="11143-102">ICorDebugBreakpoint::Activate 方法</span><span class="sxs-lookup"><span data-stu-id="11143-102">ICorDebugBreakpoint::Activate Method</span></span>
<span data-ttu-id="11143-103">設定這個的使用中狀態`ICorDebugBreakpoint`。</span><span class="sxs-lookup"><span data-stu-id="11143-103">Sets the active state of this `ICorDebugBreakpoint`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11143-104">語法</span><span class="sxs-lookup"><span data-stu-id="11143-104">Syntax</span></span>  
  
```  
HRESULT Activate (  
    [in] BOOL bActive  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="11143-105">參數</span><span class="sxs-lookup"><span data-stu-id="11143-105">Parameters</span></span>  
 `bActive`  
 <span data-ttu-id="11143-106">[in]將此值設定為`true`來指定狀態為作用中; 否則將此值設定為`false`。</span><span class="sxs-lookup"><span data-stu-id="11143-106">[in] Set this value to `true` to specify the state as active; otherwise, set this value to `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11143-107">需求</span><span class="sxs-lookup"><span data-stu-id="11143-107">Requirements</span></span>  
 <span data-ttu-id="11143-108">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="11143-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="11143-109">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="11143-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="11143-110">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="11143-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="11143-111">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="11143-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>