---
title: ICorPublishEnum 介面
ms.date: 03/30/2017
api_name:
- ICorPublishEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum
helpviewer_keywords:
- ICorPublishEnum interface [.NET Framework debugging]
ms.assetid: 76a136b5-e444-417a-8ade-f1596d597dc7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5206b7cd07acd76237ab72268b492782ac6e49ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616715"
---
# <a name="icorpublishenum-interface"></a>ICorPublishEnum 介面
可作為抽象的基底介面，可在發佈程序和應用程式定義域的相關資訊的列舉值。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[Clone 方法](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-clone-method.md)|建立一份這`ICorPublishEnum`物件。|  
|[GetCount 方法](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-getcount-method.md)|列舉中取得的項目數。|  
|[Reset 方法](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-reset-method.md)|移動資料指標的列舉型別的開頭。|  
|[Skip 方法](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-skip-method.md)|將游標移往前列舉中所指定的項目數。|  
  
## <a name="remarks"></a>備註  
 下列的列舉值衍生自`ICorPublishEnum`:  
  
-   [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md)  
  
-   [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md)  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorPub.idl CorPub.h  
  
 **程式庫：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [CorpubPublish Coclass](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
- [偵錯介面](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
