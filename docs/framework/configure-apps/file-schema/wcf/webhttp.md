---
title: <webHttp>
ms.date: 03/30/2017
ms.assetid: 1f9d0754-d41e-44ce-a298-e51cb3096c64
ms.openlocfilehash: ca6d401109d14ce11dcd40c393cd079170e4d20d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259862"
---
# <a name="webhttp"></a>\<webHttp>
此項目透過組態指定端點上的 <xref:System.ServiceModel.Description.WebHttpBehavior>。 這項行為，當搭配[ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)標準繫結，可讓 Windows Communication Foundation (WCF) 服務的 Web 程式設計模型。  
  
 \<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<webHttp>  
  
## <a name="syntax"></a>語法  
  
```xml  
<webHttp />
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|automaticFormatSelectionEnabled|當此屬性設定為 `true` 時，WCF 基礎結構會判斷要使用的最佳格式。 為了提供回溯相容性，自動格式選取預設為停用。 自動格式選取可以透過程式設計方式或透過組態啟用。|  
|defaultBodyStyle|指定傳回訊息的預設本文樣式。 如需詳細資訊，請參閱 <<c0> <xref:System.ServiceModel.Web.WebMessageBodyStyle> 並[WCF Web HTTP 格式化](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md)。|  
|defaultOutgoingResponseFormat|指定訊息的預設傳出回應格式。 如需詳細資訊，請參閱 < [WCF Web HTTP 格式化](../../../../../docs/framework/wcf/feature-details/wcf-web-http-formatting.md)。|  
|faultExceptionEnabled|取得或設定旗標，指定是否要在內部伺服器錯誤 (HTTP 狀態碼：500) 發生時產生 FaultException。|  
|helpEnabled|取得或設定值，這個值會判斷是否已啟用說明頁面。|  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|指定端點行為組。|  
  
## <a name="see-also"></a>另請參閱
- <xref:System.ServiceModel.Configuration.WebHttpElement>
- <xref:System.ServiceModel.Description.WebHttpBehavior>
- [AJAX 整合與 JSON 支援](../../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md)
- [\<webHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)
