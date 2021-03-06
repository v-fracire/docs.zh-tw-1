---
title: HOW TO：取得和設定 Windows Form DataGridView 控制項中的目前儲存格
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], getting current cell
- DataGridView control [Windows Forms], setting current cell
- cells [Windows Forms], getting and setting current
ms.assetid: b0e41e57-493a-4bd0-9376-a6f76723540c
ms.openlocfilehash: 2508551cd4bcb056d1e746b2dc962c4500093ea5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495600"
---
# <a name="how-to-get-and-set-the-current-cell-in-the-windows-forms-datagridview-control"></a>HOW TO：取得和設定 Windows Form DataGridView 控制項中的目前儲存格
互動<xref:System.Windows.Forms.DataGridView>通常會要求您以程式設計方式探索哪些儲存格是目前作用中。 此外，您可能也需要變更目前的儲存格。 您可以執行這些工作與<xref:System.Windows.Forms.DataGridView.CurrentCell%2A>屬性。  
  
> [!NOTE]
>  您無法設定目前的儲存格的資料列或資料行中其<xref:System.Windows.Forms.DataGridViewBand.Visible%2A>屬性設定為`false`。  
  
 取決於<xref:System.Windows.Forms.DataGridView>控制項的選取模式中，變更目前的儲存格可以變更選取項目。 如需詳細資訊，請參閱 < [Windows Forms DataGridView 控制項中的選取模式](../../../../docs/framework/winforms/controls/selection-modes-in-the-windows-forms-datagridview-control.md)。  
  
### <a name="to-get-the-current-cell-programmatically"></a>若要以程式設計方式取得目前的儲存格  
  
-   使用<xref:System.Windows.Forms.DataGridView>控制項的<xref:System.Windows.Forms.DataGridView.CurrentCell%2A>屬性。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#080](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#080)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#080](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#080)]  
  
### <a name="to-set-the-current-cell-programmatically"></a>以程式設計方式設定目前的儲存格  
  
-   設定<xref:System.Windows.Forms.DataGridView.CurrentCell%2A>屬性<xref:System.Windows.Forms.DataGridView>控制項。 在下列程式碼範例中，目前儲存格是設定為 0，資料行 1 的資料列。  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#085](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#085)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#085](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#085)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   <xref:System.Windows.Forms.Button> 名為的控制項`getCurrentCellButton`和`setCurrentCellButton`。 在視覺效果C#，您必須將附加<xref:System.Windows.Forms.Control.Click>相關聯的事件處理常式的範例程式碼中的每個按鈕的事件。  
  
-   名為 `dataGridView1` 的 <xref:System.Windows.Forms.DataGridView> 控制項。  
  
-   <xref:System?displayProperty=nameWithType> 和 <xref:System.Windows.Forms?displayProperty=nameWithType> 組件的參考。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.CurrentCell%2A?displayProperty=nameWithType>
- [Windows Forms DataGridView 控制項中的基本資料行、資料列和儲存格功能](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)
- [Windows Forms DataGridView 控制項中的選取模式](../../../../docs/framework/winforms/controls/selection-modes-in-the-windows-forms-datagridview-control.md)
