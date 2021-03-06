---
title: 屬性 '<propertyname>' 不會在所有程式碼路徑上傳回值
ms.date: 07/20/2015
f1_keywords:
- bc42107
- vbc42107
helpviewer_keywords:
- BC42107
ms.assetid: 06800966-9c3b-4844-9f13-83ac95607d32
ms.openlocfilehash: 1788d06aa5236d4cfc33999df86ad72c420b41df
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2019
ms.locfileid: "55268999"
---
# <a name="property-propertyname-doesnt-return-a-value-on-all-code-paths"></a>屬性 '\<屬性名稱 >' 並未傳回有關所有程式碼路徑的值
屬性 '\<屬性名稱 >' 並未傳回有關所有程式碼路徑的值。 使用結果時，Null 參考例外狀況可能在執行階段時發生。  
  
 屬性`Get`程序中的至少一個通過程式碼不會傳回值的可能的路徑。  
  
 您可以從屬性傳回值`Get`程序，在下列任一方式：  
  
-   將值指派給屬性名稱，然後再執行`Exit Property`陳述式。  
  
-   將值指派給屬性名稱，然後再執行`End Get`陳述式。  
  
-   包含值[Return 陳述式](../../../visual-basic/language-reference/statements/return-statement.md)。  
  
 如果控制權傳遞給`Exit Property`或是`End Get`和您不指派任何值給屬性名稱，`Get`程序會傳回屬性的資料類型的預設值。 如需詳細資訊，請參閱 「 行為 」 中[Function 陳述式](../../../visual-basic/language-reference/statements/function-statement.md)。  
  
 根據預設，這個訊息是一個警告。 如需隱藏警告或將警告視為錯誤的詳細資訊，請參閱 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。  
  
 **錯誤 ID:** BC42107  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
-   檢查控制項流程邏輯，並確定您指定的值會導致傳回每個陳述式之前。  
  
     很容易就能保證每一次從程序傳回將傳回值，如果您總是使用`Return`陳述式。 如果您這麼做，最後一個陳述式前面`End Get`應該是`Return`陳述式。  
  
## <a name="see-also"></a>另請參閱
- [屬性程序](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [Property 陳述式](../../../visual-basic/language-reference/statements/property-statement.md)
- [Get 陳述式](../../../visual-basic/language-reference/statements/get-statement.md)
