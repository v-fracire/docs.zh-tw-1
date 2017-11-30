---
title: "CloseCLREnumeration 函式"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CloseCLREnumeration
api_location: dbgshim.dll
api_type: COM
f1_keywords: CloseCLREnumeration
helpviewer_keywords:
- debugging API [Silverlight]
- Silverlight, debugging
- CloseCLR Enumeration function
ms.assetid: 5e3c3958-80bb-43b1-a96b-dd3e6dbd9cd7
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d9f14b851795c92c3ce0c1e7536a4ff78fbdf927
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="closeclrenumeration-function"></a><span data-ttu-id="48a65-102">CloseCLREnumeration 函式</span><span class="sxs-lookup"><span data-stu-id="48a65-102">CloseCLREnumeration Function</span></span>
<span data-ttu-id="48a65-103">關閉任何有效 common language runtime (CLR) 繼續-啟動事件所傳回的控制代碼陣列中[EnumerateCLRs 函式](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)，並釋放用於控制代碼和字串路徑陣列的記憶體。</span><span class="sxs-lookup"><span data-stu-id="48a65-103">Closes any valid common language runtime (CLR) continue-startup events located in an array of handles returned by the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md), and frees the memory for the handle and string path arrays.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48a65-104">語法</span><span class="sxs-lookup"><span data-stu-id="48a65-104">Syntax</span></span>  
  
```  
HRESULT CloseCLREnumeration (  
    [in]  DWORD      pHandleArray,  
    [in]  LPWSTR**   pStringArray,  
    [in]  DWORD*     dwArrayLength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="48a65-105">參數</span><span class="sxs-lookup"><span data-stu-id="48a65-105">Parameters</span></span>  
 `pHandleArray`  
 <span data-ttu-id="48a65-106">[in]從傳回的事件控制代碼陣列指標[EnumerateCLRs 函式](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)。</span><span class="sxs-lookup"><span data-stu-id="48a65-106">[in] Pointer to the array of event handles returned from the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md).</span></span>  
  
 `pStringArray`  
 <span data-ttu-id="48a65-107">[in]傳回從 CLR 字串路徑陣列的指標[EnumerateCLRs 函式](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)。</span><span class="sxs-lookup"><span data-stu-id="48a65-107">[in] Pointer to the array of CLR string paths returned from the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md).</span></span>  
  
 `dwArrayLength`  
 <span data-ttu-id="48a65-108">[in] 包含 `pHandleArray` 或 `pStringArray` 之大小 (長度) (兩者相同) 的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="48a65-108">[in] DWORD that contains the size (length) of either `pHandleArray` or `pStringArray` (they are the same).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="48a65-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="48a65-109">Return Value</span></span>  
 <span data-ttu-id="48a65-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="48a65-110">S_OK</span></span>  
 <span data-ttu-id="48a65-111">開啟控制代碼[EnumerateCLRs 函式](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)已關閉，並釋放用於控制代碼和字串陣列配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="48a65-111">Handles opened by the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md) are closed, and memory allocated for the handle and string arrays is freed.</span></span>  
  
 <span data-ttu-id="48a65-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="48a65-112">E_INVALIDARG</span></span>  
 <span data-ttu-id="48a65-113">`pHandleArray` 的長度不符合以 `dwArrayLength` 傳遞的長度。</span><span class="sxs-lookup"><span data-stu-id="48a65-113">The length of `pHandleArray` does not match the length that is passed in `dwArrayLength`.</span></span>  
  
 <span data-ttu-id="48a65-114">E_FAIL (或其他 E_ 傳回碼)</span><span class="sxs-lookup"><span data-stu-id="48a65-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="48a65-115">這個函式無法釋放用於 `pHandleArray` 和 `pStringArray` 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="48a65-115">The function is unable to free the memory for `pHandleArray` and `pStringArray`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48a65-116">需求</span><span class="sxs-lookup"><span data-stu-id="48a65-116">Requirements</span></span>  
 <span data-ttu-id="48a65-117">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="48a65-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48a65-118">**標頭：** dbgshim.h</span><span class="sxs-lookup"><span data-stu-id="48a65-118">**Header:** dbgshim.h</span></span>  
  
 <span data-ttu-id="48a65-119">**程式庫：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="48a65-119">**Library:** dbgshim.dll</span></span>  
  
 <span data-ttu-id="48a65-120">**.NET framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="48a65-120">**.NET Framework Versions:** 3.5 SP1</span></span>