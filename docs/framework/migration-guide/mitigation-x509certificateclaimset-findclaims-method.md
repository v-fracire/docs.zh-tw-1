---
title: 風險降低：X509CertificateClaimSet.FindClaims 方法
ms.date: 03/30/2017
ms.assetid: ee356e3b-f932-48f5-875a-5e42340bee63
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ccc24cd494866c087860144f1720988ccfc2dfa8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536434"
---
# <a name="mitigation-x509certificateclaimsetfindclaims-method"></a>風險降低：X509CertificateClaimSet.FindClaims 方法
從以 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] 為目標的應用程式開始，<xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims%2A?displayProperty=nameWithType> 方法會嘗試使 `claimType` 引數符合其 SAN 欄位中的所有 DNS 項目。  
  
## <a name="impact"></a>影響  
 這項變更只會影響以 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] 和更新版本為目標的應用程式。  
  
 若是以舊版 .NET Framework 為目標的應用程式，則 <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims%2A?displayProperty=nameWithType> 方法僅會嘗試使 `claimType` 引數符合最後一個 DNS 項目。  
  
## <a name="mitigation"></a>緩和  
 如果這不是您要的變更，以 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] 和更新版本為目標的應用程式，可以藉由將下列組態設定新增至應用程式組態檔的 [\<執行階段>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 區段，來選擇退出這項行為：  
  
```xml  
<runtime>  
   <AppContextSwitchOverrides value="Switch.System.IdentityModel.DisableMultipleDNSEntriesInSANCertificate=true" />   
</runtime>  
```  
  
 此外，以舊版 .NET Framework 為目標，但在 [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] 和更新版本下執行的應用程式，可以藉由將下列組態設定新增至應用程式組態檔的 [\<執行階段>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) 區段，來選擇加入這項行為：  
  
```xml  
<runtime>  
    <AppContextSwitchOverrides value="Switch.System.IdentityModel.DisableMultipleDNSEntriesInSANCertificate=false" />   
</runtime>  
```  
  
## <a name="see-also"></a>另請參閱
- [重定目標變更](../../../docs/framework/migration-guide/retargeting-changes-in-the-net-framework-4-6-1.md)
