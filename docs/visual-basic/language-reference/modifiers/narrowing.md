---
title: Narrowing (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.narrowing
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Narrowing keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: a207ee91-aca4-4771-b4e2-713f029bf2bb
ms.openlocfilehash: bd88c05f16a2027b0367effebef809cb5e5abfe8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617430"
---
# <a name="narrowing-visual-basic"></a>Narrowing (Visual Basic)
表示轉換運算子 (`CType`) 將類別或結構轉換成可能無法保留一些可能的值，原始的類別或結構的類型。  
  
## <a name="converting-with-the-narrowing-keyword"></a>轉換以縮小關鍵字  
 轉換程序必須指定`Public Shared`除了`Narrowing`。  
  
 縮小轉換執行不一定成功在執行階段，並可能會失敗或者會造成資料遺失。 範例包括`Long`來`Integer`，`String`到`Date`，並為衍生類型的基底型別。 這個最後一個轉換縮小，因為基底型別可能不會包含衍生型別的所有成員，而且不是衍生型別的執行個體。  
  
 如果`Option Strict`已`On`，使用程式碼必須使用`CType`所有的縮小轉換。  
  
 `Narrowing`關鍵字可以用在此內容中：  
  
 [Operator 陳述式](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
## <a name="see-also"></a>另請參閱
- [Operator 陳述式](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Widening](../../../visual-basic/language-reference/modifiers/widening.md)
- [擴展和縮小轉換](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [如何：定義運算子](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [CType 函式](../../../visual-basic/language-reference/functions/ctype-function.md)
- [Option Strict 陳述式](../../../visual-basic/language-reference/statements/option-strict-statement.md)
