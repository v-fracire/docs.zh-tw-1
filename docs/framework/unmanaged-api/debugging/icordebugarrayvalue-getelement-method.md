---
title: "ICorDebugArrayValue::GetElement 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugArrayValue.GetElement
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugArrayValue::GetElement
helpviewer_keywords:
- GetElement method [.NET Framework debugging]
- ICorDebugArrayValue::GetElement method [.NET Framework debugging]
ms.assetid: 7ac3cba5-c282-402e-b7ef-b46634f5176b
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5fc9671365a866c04671bca965ed43d83533f07f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugarrayvaluegetelement-method"></a><span data-ttu-id="57502-102">ICorDebugArrayValue::GetElement 方法</span><span class="sxs-lookup"><span data-stu-id="57502-102">ICorDebugArrayValue::GetElement Method</span></span>
<span data-ttu-id="57502-103">取得指定的陣列項目的值。</span><span class="sxs-lookup"><span data-stu-id="57502-103">Gets the value of the given array element.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57502-104">語法</span><span class="sxs-lookup"><span data-stu-id="57502-104">Syntax</span></span>  
  
```  
HRESULT GetElement (  
    [in]  ULONG32          cdim,  
    [in, size_is(cdim), length_is(cdim)]   
         ULONG32           indices[],  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="57502-105">參數</span><span class="sxs-lookup"><span data-stu-id="57502-105">Parameters</span></span>  
 `cdim`  
 <span data-ttu-id="57502-106">[in]這個維度的數目`ICorDebugArrayValue`物件。</span><span class="sxs-lookup"><span data-stu-id="57502-106">[in] The number of dimensions of this `ICorDebugArrayValue` object.</span></span>  
  
 <span data-ttu-id="57502-107">此值也是大小`indices`因為其大小的維度數目等於陣列`ICorDebugArrayValue`物件。</span><span class="sxs-lookup"><span data-stu-id="57502-107">This value is also the size of the `indices` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `indices`  
 <span data-ttu-id="57502-108">[in]陣列的索引值，其中每個指定的維度內的位置`ICorDebugArrayValue`物件。</span><span class="sxs-lookup"><span data-stu-id="57502-108">[in] An array of index values, each of which specifies a position within a dimension of the `ICorDebugArrayValue` object.</span></span>  
  
 <span data-ttu-id="57502-109">此值不能為 null。</span><span class="sxs-lookup"><span data-stu-id="57502-109">This value must not be null.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="57502-110">[out]ICorDebugValue 物件，表示指定的項目值的位址指標。</span><span class="sxs-lookup"><span data-stu-id="57502-110">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified element.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57502-111">需求</span><span class="sxs-lookup"><span data-stu-id="57502-111">Requirements</span></span>  
 <span data-ttu-id="57502-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="57502-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57502-113">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="57502-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="57502-114">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57502-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57502-115">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57502-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>