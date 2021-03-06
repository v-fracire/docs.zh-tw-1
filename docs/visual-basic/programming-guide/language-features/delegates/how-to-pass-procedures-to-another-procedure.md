---
title: HOW TO：傳遞至另一個程序，在 Visual Basic 中的程序
ms.date: 07/20/2015
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- delegates [Visual Basic], passing procedures
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
ms.openlocfilehash: cf5a8447cbedcd8071da98ac6763ff06eb608199
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506754"
---
# <a name="how-to-pass-procedures-to-another-procedure-in-visual-basic"></a>HOW TO：傳遞至另一個程序，在 Visual Basic 中的程序
此範例示範如何使用委派傳遞至其他程序的程序。  
  
 委派是您可以使用 Visual Basic 中的其他任何類型的類型。 `AddressOf`運算子會傳回委派物件時套用至程序名稱。  
  
 這個範例包含具有 delegate 參數可接受的另一個程序，以取得參考的程序`AddressOf`運算子。  
  
### <a name="create-the-delegate-and-matching-procedures"></a>建立委派和比對程序  
  
1.  建立名為委派`MathOperator`。  
  
     [!code-vb[VbVbalrDelegates#1](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_1.vb)]  
  
2.  建立名為程序`AddNumbers`使用參數和傳回值，符合`MathOperator`，如此一來，簽章相符。  
  
     [!code-vb[VbVbalrDelegates#2](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_2.vb)]  
  
3.  建立名為程序`SubtractNumbers`簽章符合`MathOperator`。  
  
     [!code-vb[VbVbalrDelegates#3](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_3.vb)]  
  
4.  建立名為程序`DelegateTest`會做為參數的委派。  
  
     此程序可接受的參考`AddNumbers`或是`SubtractNumbers`，因為它們的簽章相符`MathOperator`簽章。  
  
     [!code-vb[VbVbalrDelegates#4](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_4.vb)]  
  
5.  建立名為程序`Test`它會呼叫`DelegateTest`另一次使用的委派`AddNumbers`做為參數，並再次使用的委派`SubtractNumbers`做為參數。  
  
     [!code-vb[VbVbalrDelegates#5](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-pass-procedures-to-another-procedure_5.vb)]  
  
     當`Test`是呼叫，它顯示的第一次的結果`AddNumbers`處理`5`和`3`，這是 8。 結果`SubtractNumbers`作`9`和`3`隨即顯示，這是 6。  
  
## <a name="see-also"></a>另請參閱
- [委派](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [AddressOf 運算子](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Delegate 陳述式](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [如何：叫用委派方法](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
