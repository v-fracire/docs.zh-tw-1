---
title: IInstallReferenceItem::GetReference 方法
ms.date: 03/30/2017
api_name:
- IInstallReferenceItem.GetReference
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceItem::GetReference
helpviewer_keywords:
- IInstallReferenceItem::GetReference method [.NET Framework fusion]
- GetReference method [.NET Framework fusion]
ms.assetid: 8960332f-c98a-405a-ba92-7003de0c1187
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c768091f84157ea651c018fa89cdeafcce6c02df
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54537669"
---
# <a name="iinstallreferenceitemgetreference-method"></a>IInstallReferenceItem::GetReference 方法
取得指標[FUSION_INSTALL_REFERENCE](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md)所表示的結構[IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)物件。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT GetReference (  
    [out] LPFUSION_INSTALL_REFERENCE *ppRefData,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
#### <a name="parameters"></a>參數  
 `ppRefData`  
 [out]傳回`FUSION_INSTALL_REFERENCE`指標。  
  
 `dwFlags`  
 [in]保留供未來擴充。 `dwFlags` 必須是 0 （零）。  
  
 `pvReserved`  
 [in]保留供未來擴充。 `pvReserved` 必須是 null 參考。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** Fusion.h  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [IInstallReferenceItem 介面](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
- [FUSION_INSTALL_REFERENCE 結構](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md)
