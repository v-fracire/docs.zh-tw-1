---
title: "DestroyICeeFileGen 函式"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: DestroyICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type: COM
f1_keywords: DestroyICeeFileGen
helpviewer_keywords: DestroyICeeFileGen function [.NET Framework hosting]
ms.assetid: dc1e2235-e721-4cb2-a0b8-6b0c030d7bab
topic_type: apiref
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 11f0bd03532668196f85713459fe103f9120c82e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="destroyiceefilegen-function"></a><span data-ttu-id="36a38-102">DestroyICeeFileGen 函式</span><span class="sxs-lookup"><span data-stu-id="36a38-102">DestroyICeeFileGen Function</span></span>
<span data-ttu-id="36a38-103">終結[ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md)物件。</span><span class="sxs-lookup"><span data-stu-id="36a38-103">Destroys an [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) object.</span></span>  
  
 <span data-ttu-id="36a38-104">此函式中已被取代[!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]。</span><span class="sxs-lookup"><span data-stu-id="36a38-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36a38-105">語法</span><span class="sxs-lookup"><span data-stu-id="36a38-105">Syntax</span></span>  
  
```  
HRESULT DestroyICeeFileGen (  
    [in] ICeeFileGen  **ceeFileGen  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="36a38-106">參數</span><span class="sxs-lookup"><span data-stu-id="36a38-106">Parameters</span></span>  
 `ceeFileGen`  
 <span data-ttu-id="36a38-107">[in]`ICeeFileGen`終結物件。</span><span class="sxs-lookup"><span data-stu-id="36a38-107">[in] The `ICeeFileGen` object to destroy.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="36a38-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="36a38-108">Return Value</span></span>  
 <span data-ttu-id="36a38-109">這個方法會傳回標準的 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="36a38-109">This method returns standard COM error codes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="36a38-110">備註</span><span class="sxs-lookup"><span data-stu-id="36a38-110">Remarks</span></span>  
 <span data-ttu-id="36a38-111">`DestroyICeeFileGen`終結`ICeeFileGen`所建立的物件[CreateICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/createiceefilegen-function.md)函式。</span><span class="sxs-lookup"><span data-stu-id="36a38-111">`DestroyICeeFileGen` destroys the `ICeeFileGen` object created by the [CreateICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/createiceefilegen-function.md) function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36a38-112">需求</span><span class="sxs-lookup"><span data-stu-id="36a38-112">Requirements</span></span>  
 <span data-ttu-id="36a38-113">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="36a38-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36a38-114">**標頭：** ICeeFileGen.h</span><span class="sxs-lookup"><span data-stu-id="36a38-114">**Header:** ICeeFileGen.h</span></span>  
  
 <span data-ttu-id="36a38-115">**程式庫：** MSCorPE.dll</span><span class="sxs-lookup"><span data-stu-id="36a38-115">**Library:** MSCorPE.dll</span></span>  
  
 <span data-ttu-id="36a38-116">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="36a38-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36a38-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36a38-117">See Also</span></span>  
 [<span data-ttu-id="36a38-118">已被取代的 CLR 裝載函式</span><span class="sxs-lookup"><span data-stu-id="36a38-118">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)