---
title: "'Module' 陳述式只可以發生在檔案或命名空間層級"
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: 0820763cce9cc27f9a379ed5e766e0691a75f36b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271261"
---
# <a name="module-statements-can-occur-only-at-file-or-namespace-level"></a>'Module' 陳述式只可以發生在檔案或命名空間層級
`Module` 陳述式必須出現在原始程式檔頂端之後立即`Option`和`Imports`陳述式、 全域屬性和命名空間宣告，但所有其他宣告前面。  
  
 **錯誤 ID:** BC30617  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
-   將 `Module` 陳述式移至命名空間宣告或原始程式檔的上方。  
  
## <a name="see-also"></a>另請參閱
- [Module 陳述式](../../../visual-basic/language-reference/statements/module-statement.md)
