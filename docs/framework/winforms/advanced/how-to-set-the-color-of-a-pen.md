---
title: HOW TO：設定畫筆顏色
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- pens [Windows Forms], setting color
- colored pens
ms.assetid: a9df06f9-a6d5-4d9b-a2d1-583943540775
ms.openlocfilehash: d0402a7d6bb641ef6d97eb41bc25f3c59b3b4250
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569436"
---
# <a name="how-to-set-the-color-of-a-pen"></a>HOW TO：設定畫筆顏色
這個範例會變更預先存在的色彩<xref:System.Drawing.Pen>物件  
  
## <a name="example"></a>範例  
 [!code-cpp[System.Drawing.ConceptualHowTos#9](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#9)]
 [!code-csharp[System.Drawing.ConceptualHowTos#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#9)]
 [!code-vb[System.Drawing.ConceptualHowTos#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#9)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   A<xref:System.Drawing.Pen>名為物件`myPen`。  
  
## <a name="robust-programming"></a>穩固程式設計  
 您應該呼叫<xref:System.Drawing.Pen.Dispose%2A>耗用系統資源的物件 (例如<xref:System.Drawing.Pen>物件) 使用它們完畢之後。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Drawing.Pen>
- [圖形程式設計入門](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [如何：建立畫筆](../../../../docs/framework/winforms/advanced/how-to-create-a-pen.md)
- [使用畫筆繪製線條和形狀](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [GDI+ 中的畫筆、線條和矩形](../../../../docs/framework/winforms/advanced/pens-lines-and-rectangles-in-gdi.md)
