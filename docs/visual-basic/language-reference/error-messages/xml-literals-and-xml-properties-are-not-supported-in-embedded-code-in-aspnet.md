---
title: ASP.NET 中的內嵌式程式碼不支援 XML 常值和 XML 屬性
ms.date: 07/20/2015
f1_keywords:
- vbc31200
- bc31200
helpviewer_keywords:
- BC31200
ms.assetid: 053e8cba-8584-45cc-9fa0-43d122779772
ms.openlocfilehash: 7bec146f0100971d78eed69412ce27889e7a6263
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597160"
---
# <a name="xml-literals-and-xml-properties-are-not-supported-in-embedded-code-within-aspnet"></a>ASP.NET 中的內嵌式程式碼不支援 XML 常值和 XML 屬性
在 ASP.NET 中的內嵌程式碼中不支援 XML 常值和 XML 屬性。 若要使用 XML 功能，將移至程式碼後置的程式碼。  
  
 內嵌程式碼內定義的 XML 常值或 XML 軸屬性 (`<%= =>`) ASP.NET 檔案中。  
  
 **錯誤 ID:** BC31200  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
-   將程式碼，包括 XML 常值或 XML 軸屬性移至的 ASP.NET 程式碼後置檔案中。  
  
## <a name="see-also"></a>另請參閱
- [XML 常值](../../../visual-basic/language-reference/xml-literals/index.md)
- [XML 軸屬性](../../../visual-basic/language-reference/xml-axis/index.md)
- [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
