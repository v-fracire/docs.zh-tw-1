---
title: HOW TO：建立 GeometryDrawing
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], renderable
- renderable shapes [WPF]
- graphics [WPF], GeometryDrawing class
- classes [WPF], GeometryDrawing
ms.assetid: 11d3c096-91ba-4d41-9bba-aeac0db70f97
ms.openlocfilehash: c3312802b4a623afc10b620dbe2159d2c52a41a0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54646223"
---
# <a name="how-to-create-a-geometrydrawing"></a>HOW TO：建立 GeometryDrawing
此範例示範如何建立並顯示<xref:System.Windows.Media.GeometryDrawing>。 A<xref:System.Windows.Media.GeometryDrawing>可讓您建立與填滿外框的圖形建立關聯<xref:System.Windows.Media.Pen>並<xref:System.Windows.Media.Brush>使用<xref:System.Windows.Media.Geometry>。 <xref:System.Windows.Media.GeometryDrawing.Geometry%2A>描述圖形的結構<xref:System.Windows.Media.GeometryDrawing.Brush%2A>描述圖案的填滿，而<xref:System.Windows.Media.GeometryDrawing.Pen%2A>說明圖形外框。  
  
## <a name="example"></a>範例  
 下列範例會使用<xref:System.Windows.Media.GeometryDrawing>來轉譯圖形。 所描述的圖形<xref:System.Windows.Media.GeometryGroup>並將兩個<xref:System.Windows.Media.EllipseGeometry>物件。 用於繪製圖形的內部<xref:System.Windows.Media.LinearGradientBrush>，以繪製其外框<xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>。 <xref:System.Windows.Media.GeometryDrawing>會使用顯示<xref:System.Windows.Media.ImageDrawing>和<xref:System.Windows.Controls.Image>項目。  
  
 [!code-csharp[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/GeometryDrawingExample.cs#geometrydrawingexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/GeometryDrawingExample.xaml#geometrydrawingexamplewholepage)]  
  
 下圖顯示產生<xref:System.Windows.Media.GeometryDrawing>。  
  
 ![兩個橢圓形的 GeometryDrawing](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")  
  
 若要建立更複雜的繪圖，您可以將多個繪圖物件合併成單一複合繪圖使用<xref:System.Windows.Media.DrawingGroup>。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Media.DrawingGroup>
- [繪圖物件概觀](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [幾何概觀](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
- [建立複合圖形](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-composite-drawing.md)
