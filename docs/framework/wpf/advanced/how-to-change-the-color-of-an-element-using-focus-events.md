---
title: HOW TO：使用焦點事件變更項目的色彩
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- focus events [WPF], changing element color for
- colors of elements [WPF], changing
- elements [WPF], changing color of
ms.assetid: 7e246802-3625-47a7-ae9d-c8a2a40fd040
ms.openlocfilehash: ad5ba8490f4b98512d539f5ae9c72b03333aca69
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547010"
---
# <a name="how-to-change-the-color-of-an-element-using-focus-events"></a>HOW TO：使用焦點事件變更項目的色彩
此範例示範如何取得及使用失去焦點時，變更項目的色彩<xref:System.Windows.UIElement.GotFocus>和<xref:System.Windows.UIElement.LostFocus>事件。  
  
 此範例中組成[!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]檔案和程式碼後置檔案。  
  
## <a name="example"></a>範例  
 下列[!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)]建立使用者介面，其中包含兩個<xref:System.Windows.Controls.Button>物件，並將附加事件處理常式<xref:System.Windows.UIElement.GotFocus>並<xref:System.Windows.UIElement.LostFocus>事件<xref:System.Windows.Controls.Button>物件。  
  
 [!code-xaml[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml#gotlostfocussamplexaml)]  
  
 建立下列的程式碼後置<xref:System.Windows.UIElement.GotFocus>和<xref:System.Windows.UIElement.LostFocus>事件處理常式。  當<xref:System.Windows.Controls.Button>提升鍵盤焦點<xref:System.Windows.Controls.Control.Background%2A>的<xref:System.Windows.Controls.Button>會變成紅色。  當<xref:System.Windows.Controls.Button>失去鍵盤焦點<xref:System.Windows.Controls.Control.Background%2A>的<xref:System.Windows.Controls.Button>變更回白色。  
  
 [!code-csharp[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](../../../../samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml.cs#gotlostfocussampleeventhandlers)]
 [!code-vb[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/VisualBasic/Window1.xaml.vb#gotlostfocussampleeventhandlers)]  
  
## <a name="see-also"></a>另請參閱
- [輸入概觀](../../../../docs/framework/wpf/advanced/input-overview.md)
