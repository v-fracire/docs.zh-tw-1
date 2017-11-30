---
title: "ICorDebugChain::GetCallee 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugChain.GetCallee
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugChain::GetCallee method
helpviewer_keywords:
- ICorDebugChain::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 19560c79-abdc-4bdf-a5fe-eb362a59edc0
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ed2bf8d8e91799fd0b01012d5d6e212d26a526be
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugchaingetcallee-method"></a><span data-ttu-id="90ffd-102">ICorDebugChain::GetCallee 方法</span><span class="sxs-lookup"><span data-stu-id="90ffd-102">ICorDebugChain::GetCallee Method</span></span>
<span data-ttu-id="90ffd-103">取得由這個鏈結所呼叫。</span><span class="sxs-lookup"><span data-stu-id="90ffd-103">Gets the chain that was called by this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90ffd-104">語法</span><span class="sxs-lookup"><span data-stu-id="90ffd-104">Syntax</span></span>  
  
```  
HRESULT GetCallee (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="90ffd-105">參數</span><span class="sxs-lookup"><span data-stu-id="90ffd-105">Parameters</span></span>  
 `ppChain`  
 <span data-ttu-id="90ffd-106">[out]ICorDebugChain 物件，表示呼叫的鏈結的位址指標。</span><span class="sxs-lookup"><span data-stu-id="90ffd-106">[out] A pointer to the address of an ICorDebugChain object that represents the called chain.</span></span> <span data-ttu-id="90ffd-107">如果這個鏈結目前執行中 （也就是說，如果這個鏈結沒有在等待傳回呼叫的鏈結） 以及`ppChain`將會是 null。</span><span class="sxs-lookup"><span data-stu-id="90ffd-107">If this chain is currently executing (that is, if this chain is not waiting for a called chain to return), `ppChain` will be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="90ffd-108">備註</span><span class="sxs-lookup"><span data-stu-id="90ffd-108">Remarks</span></span>  
 <span data-ttu-id="90ffd-109">這個鏈結將會等到前它會繼續執行，傳回呼叫的鏈結。</span><span class="sxs-lookup"><span data-stu-id="90ffd-109">This chain will wait for the called chain to return before it resumes execution.</span></span> <span data-ttu-id="90ffd-110">呼叫的鏈結可能會在跨執行緒封送處理呼叫的情況下的另一個執行緒上。</span><span class="sxs-lookup"><span data-stu-id="90ffd-110">The called chain may be on another thread in the case of cross-thread marshaled calls.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90ffd-111">需求</span><span class="sxs-lookup"><span data-stu-id="90ffd-111">Requirements</span></span>  
 <span data-ttu-id="90ffd-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="90ffd-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90ffd-113">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="90ffd-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="90ffd-114">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="90ffd-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="90ffd-115">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="90ffd-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>