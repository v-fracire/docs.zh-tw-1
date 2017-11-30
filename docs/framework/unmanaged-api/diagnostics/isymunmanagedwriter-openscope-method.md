---
title: "ISymUnmanagedWriter::OpenScope 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedWriter.OpenScope
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedWriter::OpenScope
helpviewer_keywords:
- OpenScope method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::OpenScope method [.NET Framework debugging]
ms.assetid: dbea0644-3873-4329-90b8-624163e87467
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: f56bc14b096b5086db1fc8d046ed699559381fb0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedwriteropenscope-method"></a><span data-ttu-id="ae3de-102">ISymUnmanagedWriter::OpenScope 方法</span><span class="sxs-lookup"><span data-stu-id="ae3de-102">ISymUnmanagedWriter::OpenScope Method</span></span>
<span data-ttu-id="ae3de-103">開啟目前方法中的新語彙範圍。</span><span class="sxs-lookup"><span data-stu-id="ae3de-103">Opens a new lexical scope in the current method.</span></span> <span data-ttu-id="ae3de-104">範圍會變成新的目前範圍，並且推送至堆疊的範圍。</span><span class="sxs-lookup"><span data-stu-id="ae3de-104">The scope becomes the new current scope and is pushed onto a stack of scopes.</span></span> <span data-ttu-id="ae3de-105">範圍必須形成階層。</span><span class="sxs-lookup"><span data-stu-id="ae3de-105">Scopes must form a hierarchy.</span></span> <span data-ttu-id="ae3de-106">同層級不允許重疊。</span><span class="sxs-lookup"><span data-stu-id="ae3de-106">Siblings are not allowed to overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae3de-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae3de-107">Syntax</span></span>  
  
```  
HRESULT OpenScope(  
    [in] ULONG32 startOffset,  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae3de-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae3de-108">Parameters</span></span>  
 `startOffset`  
 <span data-ttu-id="ae3de-109">[in]第一個指示中的語彙範圍，以位元組為單位，從方法開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="ae3de-109">[in] The offset of the first instruction in the lexical scope, in bytes, from the beginning of the method.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="ae3de-110">[out]指標`ULONG32`接收範圍識別項。</span><span class="sxs-lookup"><span data-stu-id="ae3de-110">[out] A pointer to a `ULONG32` that receives the scope identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ae3de-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae3de-111">Return Value</span></span>  
 <span data-ttu-id="ae3de-112">如果方法成功則為 S_OK否則，E_FAIL 或其他錯誤程式碼。</span><span class="sxs-lookup"><span data-stu-id="ae3de-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae3de-113">備註</span><span class="sxs-lookup"><span data-stu-id="ae3de-113">Remarks</span></span>  
 <span data-ttu-id="ae3de-114">`ISymUnmanagedWriter::OpenScope`傳回可以搭配使用的不透明範圍識別項[isymunmanagedwriter:: Setscoperange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md)定義範圍的開始和結束位移的稍後時間。</span><span class="sxs-lookup"><span data-stu-id="ae3de-114">`ISymUnmanagedWriter::OpenScope` returns an opaque scope identifier that can be used with [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) to define a scope's starting and ending offset at a later time.</span></span> <span data-ttu-id="ae3de-115">在此情況下，位移傳遞到`ISymUnmanagedWriter::OpenScope`和[isymunmanagedwriter:: Closescope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md)都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="ae3de-115">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and [ISymUnmanagedWriter::CloseScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md) are ignored.</span></span> <span data-ttu-id="ae3de-116">範圍識別項會在目前的方法中才有效。</span><span class="sxs-lookup"><span data-stu-id="ae3de-116">Scope identifiers are valid only in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae3de-117">需求</span><span class="sxs-lookup"><span data-stu-id="ae3de-117">Requirements</span></span>  
 <span data-ttu-id="ae3de-118">**標頭：**於 CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ae3de-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae3de-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae3de-119">See Also</span></span>  
 [<span data-ttu-id="ae3de-120">ISymUnmanagedWriter 介面</span><span class="sxs-lookup"><span data-stu-id="ae3de-120">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)