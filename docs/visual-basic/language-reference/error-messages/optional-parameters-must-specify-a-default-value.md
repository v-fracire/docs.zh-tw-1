---
title: 選擇性參數必須指定預設值
ms.date: 07/20/2015
f1_keywords:
- vbc30812
- bc30812
helpviewer_keywords:
- BC30812
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
ms.openlocfilehash: dbbcc748a65942e3a89785b267e9231f4a4a01a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686175"
---
# <a name="optional-parameters-must-specify-a-default-value"></a>選擇性參數必須指定預設值
選擇性參數必須提供預設值，如果未提供參數呼叫程序可以使用。  
  
 **錯誤 ID:** BC30812  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
-   指定選擇性參數，預設的值例如：  
  
    ```  
    Sub Proc1(ByVal X As Integer,   
          Optional ByVal Y As String = "Default Value")  
       MsgBox("Default argument is: " & Y)  
    End Sub  
    ```  
  
## <a name="see-also"></a>另請參閱
- [Optional](../../../visual-basic/language-reference/modifiers/optional.md)
