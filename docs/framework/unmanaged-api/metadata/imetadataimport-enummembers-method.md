---
title: IMetaDataImport::EnumMembers 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMembers
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMembers
helpviewer_keywords:
- IMetaDataImport::EnumMembers method [.NET Framework metadata]
- EnumMembers method [.NET Framework metadata]
ms.assetid: 3fb8e178-342b-4c89-9bcf-f7f834e6cb77
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 88b8f874400d68110fa5e8fb66ca910b8e7231e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645960"
---
# <a name="imetadataimportenummembers-method"></a>IMetaDataImport::EnumMembers 方法
列舉代表指定類型成員的 MemberDef 語彙基元。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT EnumMembers (   
   [in, out]  HCORENUM    *phEnum,   
   [in]  mdTypeDef   cl,   
   [out] mdToken     rMembers[],   
   [in]  ULONG       cMax,   
   [out] ULONG       *pcTokens  
);  
```  
  
#### <a name="parameters"></a>參數  
 `phEnum`  
 [in、 out]列舉值的指標。  
  
 `cl`  
 [in]代表其成員的列舉的類型的 TypeDef 語彙基元。  
  
 `rMembers`  
 [out]陣列，用來保存 MemberDef 語彙基元。  
  
 `cMax`  
 [in] `rMembers` 陣列的大小上限。  
  
 `pcTokens`  
 [out]MemberDef 語彙基元中傳回的實際數目`rMembers`。  
  
## <a name="return-value"></a>傳回值  
  
|HRESULT|描述|  
|-------------|-----------------|  
|`S_OK`|`EnumMembers` 已成功傳回。|  
|`S_FALSE`|沒有列舉 MemberDef 語彙基元。 在此情況下，`pcTokens`為零。|  
  
## <a name="remarks"></a>備註  
 列舉集合之成員的類別，當`EnumMembers`傳回直接在類別上定義的成員。 它不會傳回此類別繼承，任何成員即使類別會提供實作這些繼承的成員。 若要列舉繼承的成員，呼叫者必須明確地逐步繼承鏈結。 請注意，規則的繼承鏈結可能會不同的語言或編譯器發出的原始中繼資料而定。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** Cor.h  
  
 **程式庫：** 包含做為 MsCorEE.dll 中的資源  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [IMetaDataImport 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
