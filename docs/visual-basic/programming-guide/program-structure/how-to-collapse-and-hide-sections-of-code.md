---
title: HOW TO：摺疊和隱藏部分程式碼 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic, code collapsing
- Visual Basic, code hiding
- Visual Basic code, collapsing and hiding
ms.assetid: b770e8f5-e07d-491a-ab4b-a977980f9ba2
ms.openlocfilehash: 1282269f06f89645c213f3daaa1bd29e95a44d35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668713"
---
# <a name="how-to-collapse-and-hide-sections-of-code-visual-basic"></a>HOW TO：摺疊和隱藏部分程式碼 (Visual Basic)
`#Region`指示詞可讓您摺疊並隱藏 Visual Basic 檔案中的程式碼區段。 `#Region`指示詞可讓您使用 Visual Studio 程式碼編輯器時，指定程式碼，您可以展開或摺疊的區塊。 更容易管理而且更方便閱讀，選擇性地隱藏程式碼的功能可讓您的檔案。 如需詳細資訊，請參閱[大綱](/visualstudio/ide/outlining)。  
  
 `#Region` 指示詞支援程式碼區塊的語意，例如`#If...#End If`。 這表示它們無法開始一個區塊中，並在另一個; 結束開始和結束必須位於相同的區塊。 `#Region` 指示詞不支援在函式內。  
  
### <a name="to-collapse-and-hide-a-section-of-code"></a>若要摺疊和隱藏程式碼區段  
  
-   放置之間的程式碼區段`#Region`和`#End Region`陳述式，如下列範例所示：  
  
     [!code-vb[VbVbalrConditionalComp#6](../../../visual-basic/language-reference/directives/codesnippet/VisualBasic/how-to-collapse-and-hide-sections-of-code_1.vb)]  
  
     `#Region`區塊可以重複使用程式碼檔案中; 因此，使用者可以定義自己的程序和類別，接著可摺疊區塊。 `#Region` 區塊也能在其他巢狀`#Region`區塊。  
  
    > [!NOTE]
    >  隱藏程式碼不會防止它正在進行編譯，並不會影響`#If...#End If`陳述式。  
  
## <a name="see-also"></a>另請參閱
- [條件式編譯](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
- [#Region 指示詞](../../../visual-basic/language-reference/directives/region-directive.md)
- [#If...Then...#Else 指示詞](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
- [大綱](/visualstudio/ide/outlining)
