---
title: Microsoft.Transactions.TransactionBridge.ReplayMessageRetry
ms.date: 03/30/2017
ms.assetid: e5b820ae-504d-405a-926a-9effa41d2369
ms.openlocfilehash: bb7f6fcf95d1ff253fa0e2963610bee2b65ef3c2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597108"
---
# <a name="microsofttransactionstransactionbridgereplaymessageretry"></a>Microsoft.Transactions.TransactionBridge.ReplayMessageRetry
重新執行訊息重試已傳送給沒有回應的協調器。  
  
## <a name="description"></a>描述  
 追蹤本機交易管理員是否因為上層協調器未在指定時間內接收到回應，而需要重新傳送「重新執行」訊息給上層協調器。  
  
## <a name="troubleshooting"></a>疑難排解  
 調查讓回應無法準時傳遞的潛在網路或產品問題。  如果看到許多這類訊息，這可能表示基礎結構發生問題或回應時間異常地長。 這兩個問題都會大幅降低系統內的異動量。  
  
## <a name="see-also"></a>另請參閱
- [追蹤](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [使用追蹤為應用程式進行疑難排解](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [管理與診斷](../../../../../docs/framework/wcf/diagnostics/index.md)
