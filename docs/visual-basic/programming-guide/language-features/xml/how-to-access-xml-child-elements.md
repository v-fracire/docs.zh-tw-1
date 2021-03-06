---
title: HOW TO：存取 XML 子項目 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- XML axis [Visual Basic], child
- child axis property [Visual Basic]
- XML child axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: 6689eb36-c471-469f-a82d-099ab8197b25
ms.openlocfilehash: 92ecea2c2e6e117add37b30498f5fb34adfeac6e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626650"
---
# <a name="how-to-access-xml-child-elements-visual-basic"></a>HOW TO：存取 XML 子項目 (Visual Basic)
此範例會示範如何使用子系軸屬性，來存取所有的 XML 子項目中的 XML 項目具有指定的名稱。 特別是，它會使用<xref:System.Xml.Linq.XElement.Value%2A>屬性的第一個項目值取得集合中`name`子軸屬性傳回。 `name`子軸屬性會取得所有子項目`phone`在`contact`物件。 此範例也會使用`phone`子軸屬性，來存取所有的子項目，名為`phone`包含在`contact`物件。  
  
## <a name="example"></a>範例  
 [!code-vb[VbXMLSamples#10](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-access-xml-child-elements_1.vb)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   <xref:System.Xml.Linq> 命名空間的參考。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Xml.Linq.XContainer.Elements%2A?displayProperty=nameWithType>
- [XML 子代軸屬性](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)
- [XML Value 屬性](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md)
- [在 Visual Basic 中存取 XML](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)
- [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)
