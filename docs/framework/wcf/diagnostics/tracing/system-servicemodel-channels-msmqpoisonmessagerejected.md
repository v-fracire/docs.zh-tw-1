---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: c8e476ab90fda9214831fbd5beaba518f3e3bd20
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491424"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a>System.ServiceModel.Channels.MsmqPoisonMessageRejected
已拒絕有害訊息。  
  
## <a name="description"></a>描述  
 此追蹤表示遇到有害訊息，隨後拒絕該訊息。 當 NetMsmqBinding 或 MsmqIntegrationBinding 上的 `ReceiveErrorHandling` 屬性設定為 `Reject` 時，便會發生這種情況。 被拒絕的訊息會傳遞回寄件者[寄不出信件佇列](https://go.microsoft.com/fwlink/?LinkId=99544)。  
  
 請參閱[有害訊息處理](https://go.microsoft.com/fwlink/?LinkId=99546)如需詳細資訊訊息何時變為有害，以及如何將服務設定為適當地處理它們。 請參閱[MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548)如需詳細資訊被拒絕的訊息表示 MSMQ 中。  
  
## <a name="see-also"></a>另請參閱
- [追蹤](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [使用追蹤為應用程式進行疑難排解](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [管理與診斷](../../../../../docs/framework/wcf/diagnostics/index.md)
- [有害訊息處理](https://go.microsoft.com/fwlink/?LinkId=99546)
- [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548)
