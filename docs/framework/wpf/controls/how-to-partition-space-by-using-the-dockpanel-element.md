---
title: HOW TO：使用 DockPanel 項目分割空間
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], partitioning space
- partitioning space [WPF]
ms.assetid: a219b9e5-b205-4438-89b5-0a137ac463ab
ms.openlocfilehash: 8b79b89e512ec9da27774188aeaeed8ebd5b1153
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577655"
---
# <a name="how-to-partition-space-by-using-the-dockpanel-element"></a>HOW TO：使用 DockPanel 項目分割空間
下列範例會建立簡易[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)]framework 使用<xref:System.Windows.Controls.DockPanel>項目。 <xref:System.Windows.Controls.DockPanel>分割可用空間，其子項目。  
  
## <a name="example"></a>範例  
 這個範例會使用<xref:System.Windows.Controls.DockPanel.Dock%2A>屬性，這是附加的屬性，將相同的兩個停駐<xref:System.Windows.Controls.Border>項目<xref:System.Windows.Controls.Dock.Top>的資料分割的空間。 第三個<xref:System.Windows.Controls.Border>元素會固定至<xref:System.Windows.Controls.Dock.Left>，使用其寬度設定為 200 像素。 第四個<xref:System.Windows.Controls.Border>停駐於<xref:System.Windows.Controls.Dock.Bottom>的畫面。 最後一個<xref:System.Windows.Controls.Border>項目會自動填滿剩餘的空間。  
  
 [!code-cpp[DockPanelOvwSample#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/DockPanelOvwSample/CPP/DockPanel_Ovw_Sample.cpp#1)]
 [!code-csharp[DockPanelOvwSample#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DockPanelOvwSample/CSharp/DockPanel_Ovw_Sample.cs#1)]
 [!code-vb[DockPanelOvwSample#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelOvwSample/VisualBasic/dockpanel_vb.vb#1)]
 [!code-xaml[DockPanelOvwSample#1](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DockPanelOvwSample/XAML/default.xaml#1)]  
  
> [!NOTE]
>  根據預設，最後一個子系<xref:System.Windows.Controls.DockPanel>項目填滿剩餘的未配置空間。 如果您不想要有此行為，請設定 `LastChildFill="False"`。  
  
 編譯後的應用程式會產生一個看起來如下的新 UI。  
  
 ![典型的 DockPanel 案例。](../../../../docs/framework/wpf/controls/media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Controls.DockPanel>
- [面板概觀](../../../../docs/framework/wpf/controls/panels-overview.md)
