---
title: "ISymUnmanagedReader2::GetMethodsInDocument 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedReader2.GetMethodsInDocument
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedReader2::GetMethodsInDocument
helpviewer_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument method [.NET Framework debugging]
- GetMethodsInDocument method [.NET Framework debugging]
ms.assetid: c7ae84d6-81e8-4cb7-a1f9-d48b6cde5d79
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 15053aeb3febd533a6977ef446fc1aa3bd8a92b8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedreader2getmethodsindocument-method"></a><span data-ttu-id="6b770-102">ISymUnmanagedReader2::GetMethodsInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="6b770-102">ISymUnmanagedReader2::GetMethodsInDocument Method</span></span>
<span data-ttu-id="6b770-103">取得具有所提供的文件中的程式行資訊的每個方法。</span><span class="sxs-lookup"><span data-stu-id="6b770-103">Gets every method that has line information in the provided document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b770-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b770-104">Syntax</span></span>  
  
```  
HRESULT GetMethodsInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is(cMethod),  
        length_is(*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6b770-105">參數</span><span class="sxs-lookup"><span data-stu-id="6b770-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="6b770-106">[in]文件指標。</span><span class="sxs-lookup"><span data-stu-id="6b770-106">[in] A pointer to the document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="6b770-107">[in]A`ULONG32`指出的大小`pRetVal`陣列。</span><span class="sxs-lookup"><span data-stu-id="6b770-107">[in] A `ULONG32` that indicates the size of the  `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="6b770-108">[out]指標`ULONG32`包含方法所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="6b770-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the methods.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="6b770-109">[out]方法會接收緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="6b770-109">[out] A pointer to the buffer that receives the methods.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6b770-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b770-110">Return Value</span></span>  
 <span data-ttu-id="6b770-111">如果方法成功則為 S_OK否則，E_FAIL 或其他錯誤程式碼。</span><span class="sxs-lookup"><span data-stu-id="6b770-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b770-112">需求</span><span class="sxs-lookup"><span data-stu-id="6b770-112">Requirements</span></span>  
 <span data-ttu-id="6b770-113">**標頭：**於 CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6b770-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b770-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b770-114">See Also</span></span>  
 [<span data-ttu-id="6b770-115">ISymUnmanagedReader2 介面</span><span class="sxs-lookup"><span data-stu-id="6b770-115">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)