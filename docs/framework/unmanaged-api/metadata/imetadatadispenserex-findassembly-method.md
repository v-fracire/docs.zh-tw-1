---
title: IMetaDataDispenserEx::FindAssembly 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssembly
helpviewer_keywords:
- FindAssembly method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssembly method [.NET Framework metadata]
ms.assetid: 3afe7252-5f28-48d9-a74d-1927566c404c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5b35abe6a11b96a88bdd610a4018469bf747fe90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550704"
---
# <a name="imetadatadispenserexfindassembly-method"></a>IMetaDataDispenserEx::FindAssembly 方法
這個方法尚未實作。 如果呼叫，它會傳回 E_NOTIMPL。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT FindAssembly(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
#### <a name="parameters"></a>參數  
 `szAppBase`  
 [in]不使用。  
  
 `szPrivateBin`  
 [in]不使用。  
  
 `szGlobalBin`  
 [in]不使用。  
  
 `szAssemblyName`  
 [in]要找的組件。  
  
 `szName`  
 [out]組件的簡單名稱。  
  
 `cchName`  
 [in]大小，以位元組為單位的`szName`。  
  
 `pcName`  
 [out]中實際傳回的字元數`szName`。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** Cor.h  
  
 **程式庫：** 做為 MsCorEE.dll 中的資源  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [IMetaDataDispenserEx 介面](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [IMetaDataDispenser 介面](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
