---
title: HOW TO：請確定多個控制項繫結至相同的資料來源都能保持同步
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], binding multiple
- controls [Windows Forms], synchronizing with data source
ms.assetid: c2f0ecc6-11e6-4c2c-a1ca-0759630c451e
ms.openlocfilehash: c6930acb57aa3c311c76b1a2acd3bbca213d1f24
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558887"
---
# <a name="how-to-ensure-multiple-controls-bound-to-the-same-data-source-remain-synchronized"></a>HOW TO：請確定多個控制項繫結至相同的資料來源都能保持同步
使用 Windows Form 中的資料繫結時，有時候多個控制項繫結至相同的資料來源中。 在某些情況下，可能必須採取額外步驟以確保控制項的繫結的內容維持彼此以及與資料來源同步處理。 這些步驟會需要有兩種情況：  
  
-   如果資料來源不會實作<xref:System.ComponentModel.IBindingList>，並因此產生<xref:System.ComponentModel.IBindingList.ListChanged>類型的事件<xref:System.ComponentModel.ListChangedType.ItemChanged>。  
  
-   如果資料來源實作<xref:System.ComponentModel.IEditableObject>。  
  
 在前一個案例中，您可以使用<xref:System.Windows.Forms.BindingSource>繫結至控制項的資料來源。 在後者的情況下，您可以使用<xref:System.Windows.Forms.BindingSource>，並處理<xref:System.Windows.Forms.BindingSource.BindingComplete>事件，並呼叫<xref:System.Windows.Forms.BindingManagerBase.EndCurrentEdit%2A>相關<xref:System.Windows.Forms.BindingManagerBase>。  
  
## <a name="example"></a>範例  
 下列程式碼範例示範如何將三個控制項繫結 — 兩個文字方塊控制項和<xref:System.Windows.Forms.DataGridView>控制 — 中的相同資料行<xref:System.Data.DataSet>使用<xref:System.Windows.Forms.BindingSource>元件。 此範例示範如何處理<xref:System.Windows.Forms.BindingSource.BindingComplete>事件，並確保其中一個文字方塊的文字值變更時，其他的文字方塊和<xref:System.Windows.Forms.DataGridView>控制項以正確的值更新。  
  
 此範例會使用<xref:System.Windows.Forms.BindingSource>繫結資料來源和控制項。 或者，您可以直接繫結控制項至資料來源，並擷取<xref:System.Windows.Forms.BindingManagerBase>從表單的繫結<xref:System.Windows.Forms.Control.BindingContext%2A>，然後處理<xref:System.Windows.Forms.BindingManagerBase.BindingComplete>事件<xref:System.Windows.Forms.BindingManagerBase>。 如何執行這項操作的範例，請參閱 [說明] 頁面，關於<xref:System.Windows.Forms.BindingManagerBase.BindingComplete>事件的<xref:System.Windows.Forms.BindingManagerBase>。  
  
 [!code-csharp[System.Windows.Forms.BindingSourceMultipleControls#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleControls/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingSourceMultipleControls#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleControls/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
  
-   此程式碼範例需要  
  
-   <xref:System>、<xref:System.Windows.Forms> 和 <xref:System.Drawing> 組件的參考。  
  
-   使用表單<xref:System.Windows.Forms.Form.Load>處理的事件和呼叫`InitializeControlsAndDataSource`方法，在範例中，從表單的<xref:System.Windows.Forms.Form.Load>事件處理常式。  
  
## <a name="see-also"></a>另請參閱
- [如何：使用 BindingSource 元件跨表單共用繫結的資料](../../../docs/framework/winforms/controls/how-to-share-bound-data-across-forms-using-the-bindingsource-component.md)
- [Windows Forms 資料繫結中的變更告知](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)
- [與資料繫結相關的介面](../../../docs/framework/winforms/interfaces-related-to-data-binding.md)
- [Windows Forms 資料繫結](../../../docs/framework/winforms/windows-forms-data-binding.md)
