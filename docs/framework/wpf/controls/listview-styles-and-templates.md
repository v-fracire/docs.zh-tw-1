---
title: ListView 樣式和範本
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ListView
- states [WPF], ListView
- ControlTemplate [WPF], ListView
- styles [WPF], ListView
- ListView [WPF], styles and templates
- templates [WPF], ListView
ms.assetid: d2387356-2171-4785-822a-7247e024b4ee
ms.openlocfilehash: 66e9f5d45a4c9b3a04291a8ebbf054ebc055b5a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643633"
---
# <a name="listview-styles-and-templates"></a>ListView 樣式和範本
本主題描述的樣式和範本<xref:System.Windows.Controls.ListView>控制項。 您可以修改預設<xref:System.Windows.Controls.ControlTemplate>，讓控制項的獨特的外觀。 如需詳細資訊，請參閱[透過建立 ControlTemplate 自訂現有控制項的外觀](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)。  
  
## <a name="listview-parts"></a>ListView 組件  
 <xref:System.Windows.Controls.ListView>控制項沒有任何具名組件。  
  
 當您建立<xref:System.Windows.Controls.ControlTemplate>for <xref:System.Windows.Controls.ListView>，您的範本可能會包含<xref:System.Windows.Controls.ItemsPresenter>內<xref:System.Windows.Controls.ScrollViewer>。 (<xref:System.Windows.Controls.ItemsPresenter>會顯示在每個項目<xref:System.Windows.Controls.ListView>;<xref:System.Windows.Controls.ScrollViewer>可在控制項內捲動)。  如果<xref:System.Windows.Controls.ItemsPresenter>不是直接子系<xref:System.Windows.Controls.ScrollViewer>，您必須給予<xref:System.Windows.Controls.ItemsPresenter>名稱， `ItemsPresenter`。  
  
## <a name="listview-states"></a>ListView 狀態  
 下表列出的視覺狀態<xref:System.Windows.Controls.ListView>控制項。  
  
|VisualState 名稱|VisualStateGroup 名稱|描述|  
|-|-|-|  
|驗證|ValidationStates|控制項使用<xref:System.Windows.Controls.Validation>類別和<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`false`。|  
|InvalidFocused|ValidationStates|<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`true`已在控制項具有焦點。|  
|InvalidUnfocused|ValidationStates|<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`true`有控制項沒有焦點。|  
  
## <a name="listviewitem-parts"></a>ListViewItem 組件  
 <xref:System.Windows.Controls.ListViewItem>控制項沒有任何具名組件。  
  
## <a name="listviewitem-states"></a>ListViewItem 狀態  
 下表列出的狀態<xref:System.Windows.Controls.ListViewItem>控制項。  
  
|VisualState 名稱|VisualStateGroup 名稱|描述|  
|-|-|-|  
|一般|CommonStates|預設狀態。|  
|已停用|CommonStates|已停用控制項。|  
|MouseOver|CommonStates|滑鼠指標位於<xref:System.Windows.Controls.ComboBox>控制項。|  
|已取得焦點|FocusStates|控制項已取得焦點。|  
|未取得焦點|FocusStates|控制項未取得焦點。|  
|已選取|SelectionStates|目前選取的項目。|  
|未選取|SelectionStates|項目未獲選取。|  
|SelectedUnfocused|SelectionStates|項目已獲選取，但未取得焦點。|  
|驗證|ValidationStates|控制項使用<xref:System.Windows.Controls.Validation>類別和<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`false`。|  
|InvalidFocused|ValidationStates|<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`true`已在控制項具有焦點。|  
|InvalidUnfocused|ValidationStates|<xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType>附加的屬性是`true`有控制項沒有焦點。|  
  
## <a name="listview-controltemplate-examples"></a>ListView ControlTemplate 範例  
 下列範例示範如何定義<xref:System.Windows.Controls.ControlTemplate>針對<xref:System.Windows.Controls.ListView>控制項和其相關聯的類型。  
  
 [!code-xaml[ControlTemplateExamples#ListView](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/listview.xaml#listview)]  
  
 <xref:System.Windows.Controls.ControlTemplate>範例會使用一或多個下列的資源。  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 如需完整的範例，請參閱[使用 ControlTemplate 設定樣式範例](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [控制項的樣式和範本](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [控制項自訂](../../../../docs/framework/wpf/controls/control-customization.md)
- [樣式設定和範本化](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [透過建立 ControlTemplate 自訂現有控制項的外觀](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
