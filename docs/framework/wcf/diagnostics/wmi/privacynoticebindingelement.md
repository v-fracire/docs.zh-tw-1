---
title: PrivacyNoticeBindingElement
ms.date: 03/30/2017
ms.assetid: 0cf110b1-e25b-4d67-986b-10cb04dc4826
ms.openlocfilehash: 4bdd860304c73771933d0f8500c6003ac7692aa1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639506"
---
# <a name="privacynoticebindingelement"></a>PrivacyNoticeBindingElement
PrivacyNoticeBindingElement  
  
## <a name="syntax"></a>語法  
  
```csharp
class PrivacyNoticeBindingElement : BindingElement  
{  
  sint32 PrivacyNoticeVersion;  
  string Url;  
};  
```  
  
## <a name="methods"></a>方法  
 PrivacyNoticeBindingElement 類別並未定義任何方法。  
  
## <a name="properties"></a>屬性  
 PrivacyNoticeBindingElement 類別具有下列屬性：  
  
### <a name="privacynoticeversion"></a>PrivacyNoticeVersion  
 資料型別：sint32  
  
 存取類型：唯讀  
  
 隱私權注意事項的版本。  
  
### <a name="url"></a>URL  
 資料型別：字串  
  
 存取類型：唯讀  
  
 隱私權注意事項所在的 URL。  
  
## <a name="requirements"></a>需求  
  
|MOF|於 Servicemodel.mof 中宣告。|  
|---------|-----------------------------------|  
|命名空間|於 root\ServiceModel 中定義|  
  
## <a name="see-also"></a>另請參閱
- <xref:System.ServiceModel.Channels.PrivacyNoticeBindingElement>
