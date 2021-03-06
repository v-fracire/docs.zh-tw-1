---
title: 屬性 '<attributename>' 不可以多次套用
ms.date: 07/20/2015
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords:
- BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
ms.openlocfilehash: 62e84d174e4e218472eda9b7c08ed677e0140438
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278703"
---
# <a name="attribute-attributename-cannot-be-applied-multiple-times"></a>屬性 '\<屬性名稱 >' 不可套用多次
屬性只能套用一次。 `AttributeUsage`屬性會決定是否可以多次套用屬性。  
  
 **錯誤 ID:** BC30663  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1.  請確定屬性只能套用一次。  
  
2.  如果您使用的您開發的自訂屬性，請考慮變更其`AttributeUsage`屬性，以允許多個屬性使用方式，如同下列範例。  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.AttributeUsageAttribute>
- [建立自訂屬性](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)
- [AttributeUsage](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
