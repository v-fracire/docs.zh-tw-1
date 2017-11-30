---
title: "IMetaDataImport::EnumModuleRefs 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.EnumModuleRefs
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::EnumModuleRefs
helpviewer_keywords:
- EnumModuleRefs method [.NET Framework metadata]
- IMetaDataImport::EnumModuleRefs method [.NET Framework metadata]
ms.assetid: 53441f3a-68d2-477c-906e-37c55dfcfb4d
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ebba448881b934220f0eb46c392ab0909ae37f68
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportenummodulerefs-method"></a><span data-ttu-id="bc257-102">IMetaDataImport::EnumModuleRefs 方法</span><span class="sxs-lookup"><span data-stu-id="bc257-102">IMetaDataImport::EnumModuleRefs Method</span></span>
<span data-ttu-id="bc257-103">列舉代表已匯入的模組之 ModuleRef 語彙基元。</span><span class="sxs-lookup"><span data-stu-id="bc257-103">Enumerates ModuleRef tokens that represent imported modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc257-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc257-104">Syntax</span></span>  
  
```  
HRESULT EnumModuleRefs (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdModuleRef  rModuleRefs[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcModuleRefs  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bc257-105">參數</span><span class="sxs-lookup"><span data-stu-id="bc257-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="bc257-106">[in、 out]列舉值的指標。</span><span class="sxs-lookup"><span data-stu-id="bc257-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="bc257-107">這必須是 NULL 的第一個呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="bc257-107">This must be NULL for the first call of this method.</span></span>  
  
 `rModuleRefs`  
 <span data-ttu-id="bc257-108">[out]陣列，用來儲存 ModuleRef 語彙基元。</span><span class="sxs-lookup"><span data-stu-id="bc257-108">[out] The array used to store the ModuleRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="bc257-109">[in] `rModuleRefs` 陣列的大小上限。</span><span class="sxs-lookup"><span data-stu-id="bc257-109">[in] The maximum size of the `rModuleRefs` array.</span></span>  
  
 `pcModuleRefs`  
 <span data-ttu-id="bc257-110">[out]ModuleRef 語彙基元中傳回的數目`rModuleRefs`。</span><span class="sxs-lookup"><span data-stu-id="bc257-110">[out] The number of ModuleRef tokens returned in `rModuleRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bc257-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc257-111">Return Value</span></span>  
  
|<span data-ttu-id="bc257-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bc257-112">HRESULT</span></span>|<span data-ttu-id="bc257-113">說明</span><span class="sxs-lookup"><span data-stu-id="bc257-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="bc257-114">`EnumModuleRefs`已成功傳回。</span><span class="sxs-lookup"><span data-stu-id="bc257-114">`EnumModuleRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="bc257-115">沒有列舉語彙基元。</span><span class="sxs-lookup"><span data-stu-id="bc257-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="bc257-116">在此情況下，`pcModuleRefs`為零。</span><span class="sxs-lookup"><span data-stu-id="bc257-116">In that case, `pcModuleRefs` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bc257-117">需求</span><span class="sxs-lookup"><span data-stu-id="bc257-117">Requirements</span></span>  
 <span data-ttu-id="bc257-118">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bc257-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bc257-119">**標頭：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="bc257-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bc257-120">**程式庫：**包含做為 MsCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="bc257-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bc257-121">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bc257-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc257-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc257-122">See Also</span></span>  
 [<span data-ttu-id="bc257-123">IMetaDataImport 介面</span><span class="sxs-lookup"><span data-stu-id="bc257-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="bc257-124">IMetaDataImport2 介面</span><span class="sxs-lookup"><span data-stu-id="bc257-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)