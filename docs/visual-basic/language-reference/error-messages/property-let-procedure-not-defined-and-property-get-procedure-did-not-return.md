---
title: 未定義屬性 let 的程序，而屬性 get 的程序並未傳回物件
ms.date: 07/20/2015
f1_keywords:
- vbrID451
ms.assetid: 8542382a-689f-4e1b-abc0-c1e2dadb92f4
ms.openlocfilehash: 65bd2e5cf9c6bbc2d9198dd7fc8947c5a17aa9e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597134"
---
# <a name="property-let-procedure-not-defined-and-property-get-procedure-did-not-return-an-object"></a>未定義屬性 let 的程序，而屬性 get 的程序並未傳回物件
特定屬性、 方法和作業只能套用至`Collection`物件。 您指定的作業或是專為集合的屬性，但該物件不是集合。  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1.  物件或屬性名稱的拼字檢查或確認物件是否`Collection`物件。  
  
2.  看看`Add`方法用來將物件加入至集合，以便能確定語法是否正確，以及任何識別項的拼字是否正確。  
  
## <a name="see-also"></a>另請參閱
- <xref:Microsoft.VisualBasic.Collection>
