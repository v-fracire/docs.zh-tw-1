---
title: marshalCleanupError MDA
ms.date: 03/30/2017
helpviewer_keywords:
- cleanup operations
- marshaling, run-time errors
- managed debugging assistants (MDAs), marshaling
- MDAs (managed debugging assistants), marshaling
- marshaling cleanup error
- MarshalCleanupError MDA
- memory, cleanup errors
ms.assetid: 2f5d9e7c-ae51-4155-a435-54347aa1f091
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ff7286eb104f36ceb5e1d9b30f4a265fb068d3e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564665"
---
# <a name="marshalcleanuperror-mda"></a>marshalCleanupError MDA
如果通用語言執行平台 (CLR) 在嘗試清除用來封送處理本機與 Managed 程式碼界限間之資料類型的暫存結構和記憶體時，發生錯誤，就會啟用 `marshalCleanupError` Managed 偵錯助理 (MDA)。  
  
## <a name="symptoms"></a>徵兆  
 進行本機與 Managed 程式碼轉換時發生記憶體流失、執行緒文化特性之類的執行階段狀態未還原，或是 <xref:System.Runtime.InteropServices.SafeHandle> 清除發生錯誤。  
  
## <a name="cause"></a>原因  
 清除暫存結構時，發生非預期的錯誤。  
  
## <a name="resolution"></a>解決方式  
 檢閱所有 <xref:System.Runtime.InteropServices.SafeHandle> 建構函式、完成項和自訂封送處理器實作是否有錯誤。  
  
## <a name="effect-on-the-runtime"></a>對執行階段的影響  
 此 MDA 對 CLR 沒有影響。  
  
## <a name="output"></a>輸出  
 出現一則訊息，提報在清除期間失敗的作業。  
  
## <a name="configuration"></a>組態  
  
```xml  
<mdaConfig>  
  <assistants>  
    <marshalCleanupError />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [診斷 Managed 偵錯助理的錯誤](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [Interop 封送處理](../../../docs/framework/interop/interop-marshaling.md)
