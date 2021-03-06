---
title: HOW TO：參考目前的執行個體的物件 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: d166ce62a2bb0522d1ca7011aeff7afe076c2d8e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54542193"
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a>HOW TO：參考目前的執行個體的物件 (Visual Basic)
*目前的執行個體*物件是目前執行所在的程式碼的執行個體。  
  
 您使用`Me`關鍵字來參考目前的執行個體。  
  
### <a name="to-refer-to-the-current-instance"></a>若要參考之目前執行個體  
  
-   使用`Me`關鍵字，您通常會使用物件變數的名稱。  
  
    ```  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     雖然`Me`行為就像物件變數時，您不能宣告它或將任何項目指派給它。 `Me` 一律是指目前的執行個體。  
  
## <a name="see-also"></a>另請參閱
- [物件變數](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [物件變數指派](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Me、My、MyBase 和 MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
