---
title: CreateALink 函式
ms.date: 03/30/2017
api_name:
- CreateALink
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- CreateALink
helpviewer_keywords:
- CreateALink function
- Alink API, CreateALink function
ms.assetid: fc73bcb9-6af6-44d8-bc39-2f4400325dae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f809395de68b596f769f9396da8668bf296b1aa2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675037"
---
# <a name="createalink-function"></a>CreateALink 函式
建立組件連結器的執行個體，並將指標設定為指定的介面。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT CreateALink (  
   REFIID riid,  
   IUnknown **ppInterface  
);  
```  
  
#### <a name="parameters"></a>參數  
  
|參數|描述|  
|---------------|-----------------|  
|`riid`|其中一個組件連結器介面的實體名稱。|  
|`ppInterface`|成功完成時包含位置的指標`riid`介面。|  
  
## <a name="requirements"></a>需求  
 **程式庫**: alink.dll  
  
## <a name="see-also"></a>另請參閱
- [Al.exe (組件連結器)](../../../../docs/framework/tools/al-exe-assembly-linker.md)
