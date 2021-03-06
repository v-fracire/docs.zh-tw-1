---
title: GDI+ 中的多邊形
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- polygons
- drawing [Windows Forms], polygons
- GDI+, polygons
ms.assetid: a72213d2-d69a-4c2b-a75c-be7b20390c13
ms.openlocfilehash: 94f18b3150a5c953f2e886f644ec5cfaabd786fc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511507"
---
# <a name="polygons-in-gdi"></a>GDI+ 中的多邊形
多邊形是封閉的形狀，具有三個或多個直接邊。 例如，三角形是具有三個邊的多邊形矩形四個邊的多邊形，是五邊形是具有五個邊的多邊形。 下圖顯示幾個多邊形。  
  
 ![Polygons](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art07.gif "Aboutgdip02_art07")  
  
## <a name="drawing-a-polygon"></a>繪製多邊形  
 若要繪製多邊形，您需要<xref:System.Drawing.Graphics>物件，<xref:System.Drawing.Pen>物件和陣列<xref:System.Drawing.Point>(或<xref:System.Drawing.PointF>) 物件。 <xref:System.Drawing.Graphics>物件提供<xref:System.Drawing.Graphics.DrawPolygon%2A>方法。 <xref:System.Drawing.Pen>物件會儲存屬性，例如 寬度 和 用來呈現多邊形，且陣列線條的色彩，<xref:System.Drawing.Point>物件會儲存連接的直線，線條的點。 <xref:System.Drawing.Pen>物件和陣列<xref:System.Drawing.Point>物件會傳遞做為引數<xref:System.Drawing.Graphics.DrawPolygon%2A>方法。 下列範例會繪製三邊的多邊形。 請注意，只有三個點`myPointArray`:（0，0），（50、 30） 和 （30、 60）。 <xref:System.Drawing.Graphics.DrawPolygon%2A>方法會自動關閉多邊形，藉由繪製一條線從 （30、 60） 回到起點 （0，0）。  
  
 [!code-csharp[LinesCurvesAndShapes#111](../../../../samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#111)]
 [!code-vb[LinesCurvesAndShapes#111](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#111)]  
  
 下圖顯示多邊形。  
  
 ![Polygon](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art08.gif "Aboutgdip02_art08")  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [線條、曲線和形狀](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)
- [如何：建立畫筆](../../../../docs/framework/winforms/advanced/how-to-create-a-pen.md)
