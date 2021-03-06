---
title: HOW TO：自訂滑桿上的刻度
ms.date: 03/30/2017
helpviewer_keywords:
- TickBar [WPF]
- Slider control [WPF], creating with TickBar
ms.assetid: 4fa694f2-a620-4b15-be78-5f4286f89361
ms.openlocfilehash: b6ade07b0b4c04578d2523d6d8ba992b8b2d31f7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696668"
---
# <a name="how-to-customize-the-ticks-on-a-slider"></a>HOW TO：自訂滑桿上的刻度
此範例示範如何建立<xref:System.Windows.Controls.Slider>具有刻度標記的控制項。  
  
## <a name="example"></a>範例  
 <xref:System.Windows.Controls.Primitives.TickBar>顯示當您設定<xref:System.Windows.Controls.Slider.TickPlacement%2A>以外的值的屬性<xref:System.Windows.Controls.Primitives.TickPlacement.None>，這是預設值。  
  
 下列範例示範如何建立<xref:System.Windows.Controls.Slider>與<xref:System.Windows.Controls.Primitives.TickBar>會顯示刻度。 <xref:System.Windows.Controls.Slider.TickPlacement%2A>和<xref:System.Windows.Controls.Slider.TickFrequency%2A>屬性，定義刻度標記和它們之間的間隔的位置。 當您移動<xref:System.Windows.Controls.Primitives.Thumb>，工具提示顯示的值<xref:System.Windows.Controls.Slider>。 <xref:System.Windows.Controls.Slider.AutoToolTipPlacement%2A>屬性會定義工具提示的發生。 <xref:System.Windows.Controls.Primitives.Thumb>移動對應到刻度的位置，因為<xref:System.Windows.Controls.Slider.IsSnapToTickEnabled%2A>設定為`true`。  
  
 下列範例示範如何使用<xref:System.Windows.Controls.Slider.Ticks%2A>屬性，以建立刻度標記沿著<xref:System.Windows.Controls.Slider>以不規則的間隔。  
  
 [!code-xaml[Slider#4](../../../../samples/snippets/xaml/VS_Snippets_Wpf/Slider/xaml/window1.xaml#4)]  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Controls.Slider>
- <xref:System.Windows.Controls.Primitives.TickBar>
- <xref:System.Windows.Controls.Slider.TickPlacement%2A>
- [滑桿操作說明主題](https://msdn.microsoft.com/library/534be86c-afb2-425d-8186-631278a9925e)
