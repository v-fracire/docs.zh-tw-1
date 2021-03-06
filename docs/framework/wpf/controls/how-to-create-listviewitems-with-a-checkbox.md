---
title: HOW TO：使用 CheckBox 建立 ListViewItems
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: 1ed623495529609c83c0ced68bfc1696c29d4570
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54682238"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a>HOW TO：使用 CheckBox 建立 ListViewItems
此範例示範如何顯示的資料行<xref:System.Windows.Controls.CheckBox>中的控制項<xref:System.Windows.Controls.ListView>使用的控制項<xref:System.Windows.Controls.GridView>。  
  
## <a name="example"></a>範例  
 若要建立包含的資料行<xref:System.Windows.Controls.CheckBox>中的控制項<xref:System.Windows.Controls.ListView>，建立<xref:System.Windows.DataTemplate>包含<xref:System.Windows.Controls.CheckBox>。 然後設定<xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A>的<xref:System.Windows.Controls.GridViewColumn>至<xref:System.Windows.DataTemplate>。  
  
 下列範例所示<xref:System.Windows.DataTemplate>，其中包含<xref:System.Windows.Controls.CheckBox>。 此範例會將繫結<xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A>屬性<xref:System.Windows.Controls.CheckBox>要<xref:System.Windows.Controls.ListBoxItem.IsSelected%2A>屬性值為<xref:System.Windows.Controls.ListViewItem>包含它。 因此，當<xref:System.Windows.Controls.ListViewItem>，其中包含<xref:System.Windows.Controls.CheckBox>已選取，<xref:System.Windows.Controls.CheckBox>已核取。  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 下列範例示範如何建立的資料行<xref:System.Windows.Controls.CheckBox>控制項。 若要將資料行，範例會設定<xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A>的屬性<xref:System.Windows.Controls.GridViewColumn>至<xref:System.Windows.DataTemplate>。  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [ListView 概觀](../../../../docs/framework/wpf/controls/listview-overview.md)
- [HOW-TO 主題](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [GridView 概觀](../../../../docs/framework/wpf/controls/gridview-overview.md)
