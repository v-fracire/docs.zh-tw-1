---
title: PublicKeyBlob 結構
ms.date: 03/30/2017
api_name:
- PublicKeyBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- PublicKeyBlob
helpviewer_keywords:
- PublicKeyBlob structure [.NET Framework strong naming]
ms.assetid: b9240712-829c-4c8d-9a09-a6e7aa63f63a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1a5e18c0cf65ee8f336b74a2d8e44fcf5af0cfef
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2019
ms.locfileid: "56261774"
---
# <a name="publickeyblob-structure"></a>PublicKeyBlob 結構
以二進位格式，表示公用/私密金鑰組的公開金鑰。  
  
## <a name="syntax"></a>語法  
  
```  
typedef struct {  
    unsigned int SigAlgId;  
    unsigned int HashAlgId;  
    ULONG cbPublicKey;  
    BYTE PublicKey[1]  
} PublicKeyBlob;   
```  
  
## <a name="members"></a>成員  
  
|成員|描述|  
|------------|-----------------|  
|`SigAlgId`|簽章演算法的識別項 (型別`ALG_ID`、 WinCrypt.h 中所定義) 的公開金鑰。|  
|`HashAlgId`|雜湊演算法的識別項 (型別`ALG_ID`、 WinCrypt.h 中所定義) 的公開金鑰。|  
|`cbPublicKey`|以位元組為單位的金鑰長度。|  
|`PublicKey`|可變長度位元組陣列，其中包含的索引鍵值在 CryptoAPI 所傳回的格式。|  
  
## <a name="remarks"></a>備註  
 `PublicKeyBlob`結構由[StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md)， [StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md)，和其他的強式名稱函式，來代表公開/私密金鑰組的公開金鑰。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** StrongName.h  
  
 **程式庫：** 包含做為 MsCorEE.dll 中的資源  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [StrongNameGetPublicKey 函式](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md)
- [StrongNameSignatureGeneration 函式](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md)
