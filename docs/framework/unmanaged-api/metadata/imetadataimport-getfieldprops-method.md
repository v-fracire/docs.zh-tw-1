---
title: "IMetaDataImport::GetFieldProps 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetFieldProps
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetFieldProps
helpviewer_keywords:
- IMetaDataImport::GetFieldProps method [.NET Framework metadata]
- GetFieldProps method [.NET Framework metadata]
ms.assetid: 7b0e9b10-8cef-4ba6-8432-40bf63e65ab1
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d5874169e0f8c452b177309702444ea84858557e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportgetfieldprops-method"></a><span data-ttu-id="bd448-102">IMetaDataImport::GetFieldProps 方法</span><span class="sxs-lookup"><span data-stu-id="bd448-102">IMetaDataImport::GetFieldProps Method</span></span>
<span data-ttu-id="bd448-103">取得與指定 FieldDef 語彙基元所參考欄位相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bd448-103">Gets metadata associated with the field referenced by the specified FieldDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd448-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd448-104">Syntax</span></span>  
  
```  
HRESULT GetFieldProps (  
   [in]  mdFieldDef        mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szField,  
   [in]  ULONG             cchField,   
   [out] ULONG             *pchField,  
   [out] DWORD             *pdwAttr,  
   [in]  PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bd448-105">參數</span><span class="sxs-lookup"><span data-stu-id="bd448-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="bd448-106">[in]FieldDef 語彙基元，代表要取得相關聯的中繼資料的欄位。</span><span class="sxs-lookup"><span data-stu-id="bd448-106">[in] A FieldDef token that represents the field to get associated metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="bd448-107">[out]表示欄位所屬的類別類型的 TypeDef 語彙基元指標。</span><span class="sxs-lookup"><span data-stu-id="bd448-107">[out] A pointer to a TypeDef token that represents the type of the class that the field belongs to.</span></span>  
  
 `szField`  
 <span data-ttu-id="bd448-108">[out]欄位的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd448-108">[out] The name of the field.</span></span>  
  
 `cchField`  
 <span data-ttu-id="bd448-109">[in]寬字元的緩衝區大小*szField*。</span><span class="sxs-lookup"><span data-stu-id="bd448-109">[in] The size in wide characters of the buffer for *szField*.</span></span>  
  
 `pchField`  
 <span data-ttu-id="bd448-110">[out]實際傳回的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="bd448-110">[out] The actual size of the returned buffer.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="bd448-111">[out]欄位的中繼資料與相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="bd448-111">[out] Flags associated with the field's metadata.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="bd448-112">[in]描述欄位的二進位中繼資料值的指標。</span><span class="sxs-lookup"><span data-stu-id="bd448-112">[in] A pointer to the binary metadata value that describes the field.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="bd448-113">[out]以位元組為單位的大小`ppvSigBlob`。</span><span class="sxs-lookup"><span data-stu-id="bd448-113">[out] The size in bytes of `ppvSigBlob`.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="bd448-114">[out]指定欄位的值類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="bd448-114">[out] A flag that specifies the value type of the field.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="bd448-115">[out]欄位的常值。</span><span class="sxs-lookup"><span data-stu-id="bd448-115">[out] A constant value for the field.</span></span>  
  
 `pcchValue`  
 <span data-ttu-id="bd448-116">[out]以字元為單位的大小`ppValue`，或為零，如果字串不存在。</span><span class="sxs-lookup"><span data-stu-id="bd448-116">[out] The size in chars of `ppValue`, or zero if no string exists.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd448-117">需求</span><span class="sxs-lookup"><span data-stu-id="bd448-117">Requirements</span></span>  
 <span data-ttu-id="bd448-118">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bd448-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd448-119">**標頭：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="bd448-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bd448-120">**程式庫：**包含做為 MsCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="bd448-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bd448-121">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd448-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd448-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd448-122">See Also</span></span>  
 [<span data-ttu-id="bd448-123">IMetaDataImport 介面</span><span class="sxs-lookup"><span data-stu-id="bd448-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="bd448-124">IMetaDataImport2 介面</span><span class="sxs-lookup"><span data-stu-id="bd448-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)