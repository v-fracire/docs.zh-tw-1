---
title: "IHostFilter::MarkToken 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostFilter.MarkToken
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostFilter::MarkToken
helpviewer_keywords:
- MarkToken method, IHostFilter interface [.NET Framework metadata]
- IHostFilter::MarkToken method [.NET Framework metadata]
ms.assetid: d7061343-d0a3-4fd5-b312-61974f98bd62
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9556880ad534f5c82d8d0e874129876478e2e63f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="ihostfiltermarktoken-method"></a><span data-ttu-id="33f63-102">IHostFilter::MarkToken 方法</span><span class="sxs-lookup"><span data-stu-id="33f63-102">IHostFilter::MarkToken Method</span></span>
<span data-ttu-id="33f63-103">表示將處理指定的中繼資料語彙基元。</span><span class="sxs-lookup"><span data-stu-id="33f63-103">Indicates that the specified metadata token will be processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33f63-104">語法</span><span class="sxs-lookup"><span data-stu-id="33f63-104">Syntax</span></span>  
  
```  
HRESULT MarkToken (  
    [in]  mdToken         tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="33f63-105">參數</span><span class="sxs-lookup"><span data-stu-id="33f63-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="33f63-106">[in]要處理的中繼資料語彙基元。</span><span class="sxs-lookup"><span data-stu-id="33f63-106">[in] The metadata token to be processed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="33f63-107">備註</span><span class="sxs-lookup"><span data-stu-id="33f63-107">Remarks</span></span>  
 <span data-ttu-id="33f63-108">您通常會想要如果在中繼資料範圍內處理的語彙基元。</span><span class="sxs-lookup"><span data-stu-id="33f63-108">Typically, you want a token to be processed if it is in the metadata scope.</span></span> <span data-ttu-id="33f63-109">`MarkToken`方法傳遞至中繼資料引擎透過[imetadataemit:: Sethandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="33f63-109">The `MarkToken` method is passed to the metadata engine via the [IMetaDataEmit::SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="33f63-110">需求</span><span class="sxs-lookup"><span data-stu-id="33f63-110">Requirements</span></span>  
 <span data-ttu-id="33f63-111">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="33f63-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33f63-112">**標頭：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="33f63-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="33f63-113">**程式庫：**做為 MsCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="33f63-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="33f63-114">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33f63-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33f63-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33f63-115">See Also</span></span>  
 [<span data-ttu-id="33f63-116">中繼資料介面</span><span class="sxs-lookup"><span data-stu-id="33f63-116">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)  
 [<span data-ttu-id="33f63-117">IHostFilter 介面</span><span class="sxs-lookup"><span data-stu-id="33f63-117">IHostFilter Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/ihostfilter-interface.md)