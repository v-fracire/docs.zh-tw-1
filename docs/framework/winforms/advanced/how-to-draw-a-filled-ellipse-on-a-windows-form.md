---
title: HOW TO：Windows Form 上繪製實心的橢圓形
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.FillEllipse
helpviewer_keywords:
- ellipses [Windows Forms], drawing
- circles [Windows Forms], drawing
- circular shapes
- drawing [Windows Forms], ellipses
- shapes [Windows Forms], drawing
- forms [Windows Forms], drawing ellipses
ms.assetid: 781db806-950d-4c5b-b022-493f7fd0c4a8
ms.openlocfilehash: 09c98ec2874566cc49319d174ef7f1650a436d38
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616898"
---
# <a name="how-to-draw-a-filled-ellipse-on-a-windows-form"></a>HOW TO：Windows Form 上繪製實心的橢圓形
此範例會在表單上繪製實心的橢圓形。  
  
## <a name="example"></a>範例  
 [!code-cpp[System.Drawing.ConceptualHowTos#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#1)]
 [!code-csharp[System.Drawing.ConceptualHowTos#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#1)]
 [!code-vb[System.Drawing.ConceptualHowTos#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 您不能呼叫這個方法<xref:System.Windows.Forms.Form.Load>事件處理常式。 如果調整大小或遮蔽另一種形式的表單時，將不會重新繪製的繪製的內容。 若要讓您自動重新繪製的內容，您應該覆寫<xref:System.Windows.Forms.Control.OnPaint%2A>方法。  
  
## <a name="robust-programming"></a>穩固程式設計  
 您應該一律呼叫<xref:System.IDisposable.Dispose%2A>耗用系統資源，例如任何物件上<xref:System.Drawing.Brush>和<xref:System.Drawing.Graphics>物件。  
  
## <a name="see-also"></a>另請參閱
- [Windows Forms 中的圖形和繪圖](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [圖形程式設計入門](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [Alpha 混色線條和填色](../../../../docs/framework/winforms/advanced/alpha-blending-lines-and-fills.md)
- [使用筆刷填滿形狀](../../../../docs/framework/winforms/advanced/using-a-brush-to-fill-shapes.md)
