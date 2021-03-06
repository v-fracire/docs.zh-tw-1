---
title: AddHandler 陳述式 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AddHandlerMethod
- addhandler
- vb.addhandler
helpviewer_keywords:
- AddHandler statement [Visual Basic]
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
ms.openlocfilehash: 6ed6f3d4fd77d714ab554d641c0c0fc4f403bbf8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715097"
---
# <a name="addhandler-statement"></a>AddHandler 陳述式
將事件與事件處理常式在執行階段。  
  
## <a name="syntax"></a>語法  
  
```  
AddHandler event, AddressOf eventhandler  
```  
  
## <a name="parts"></a>組件  
|||
|---|---|
|Event - 事件|要處理的事件名稱。|  
|`eventhandler`|處理事件的程序的名稱。|
|||
  
## <a name="remarks"></a>備註  
 `AddHandler`和`RemoveHandler`陳述式可讓您能夠啟動和停止程式執行期間隨時的事件處理。  
  
 簽章`eventhandler`程序必須符合的事件簽章`event`。  
  
 `Handles` 關鍵字和 `AddHandler` 陳述式都可以讓您指定由特定程序處理特定事件，但兩者存有差異。 `AddHandler` 陳述式會在執行階段將程序連接到事件。 當定義程序以指定它處理特定事件時，使用 `Handles` 關鍵字。 如需詳細資訊，請參閱 <<c0> [ 處理](../../../visual-basic/language-reference/statements/handles-clause.md)。  
  
> [!NOTE]
>  自訂事件，如`AddHandler`陳述式會叫用事件的`AddHandler`存取子。 如需有關自訂事件的詳細資訊，請參閱 < [Event 陳述式](../../../visual-basic/language-reference/statements/event-statement.md)。  
  
## <a name="example"></a>範例  
 [!code-vb[VbVbalrEvents#17](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/addhandler-statement_1.vb)]  
  
## <a name="see-also"></a>另請參閱
- [RemoveHandler 陳述式](../../../visual-basic/language-reference/statements/removehandler-statement.md)
- [Handles](../../../visual-basic/language-reference/statements/handles-clause.md)
- [Event 陳述式](../../../visual-basic/language-reference/statements/event-statement.md)
- [事件](../../../visual-basic/programming-guide/language-features/events/index.md)
