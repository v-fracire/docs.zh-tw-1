---
title: 服務效能計數器
ms.date: 03/30/2017
ms.assetid: 4210f549-31f2-4ea7-99bd-69eaffb98ddf
ms.openlocfilehash: bf0b12e6d4954c0a1392554d7269a7d539a77dc1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545591"
---
# <a name="service-performance-counters"></a>服務效能計數器
服務效能計數器會測量整體的服務行為，而且可用於診斷整個服務的效能。 以效能監視器 (Perfmon.exe) 檢視時，可以在 `ServiceModelService 4.0.0.0` 效能物件下找到它們。 執行個體會使用以下模式來命名：  
  
```  
ServiceName@ServiceBaseAddress  
```  
  
> [!CAUTION]
>  效能計數器執行個體的名稱具有長度限制。 當 Windows Communication Foundation (WCF) 計數器執行個體名稱超過最大長度時，WCF 會以雜湊值取代一部分的執行個體名稱。  
  
## <a name="see-also"></a>另請參閱
- [效能計數器](../../../../../docs/framework/wcf/diagnostics/performance-counters/index.md)
