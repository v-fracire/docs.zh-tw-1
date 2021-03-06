---
title: ComboBox 控制項概觀 (Windows Form)
ms.date: 03/30/2017
f1_keywords:
- ComboBox
helpviewer_keywords:
- drop-down lists [Windows Forms], Windows Forms
- ComboBox control [Windows Forms], about ComboBox control
- drop-down lists [Windows Forms], ComboBox control
- combo boxes [Windows Forms], about combo boxes
ms.assetid: a58b393f-a614-45d1-8961-857a024b5acd
ms.openlocfilehash: 1c58249df67efe5e782776d4996adef567f71a15
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492205"
---
# <a name="combobox-control-overview-windows-forms"></a>ComboBox 控制項概觀 (Windows Form)
Windows Form<xref:System.Windows.Forms.ComboBox>控制項用來顯示在下拉式清單方塊中的資料。 根據預設，<xref:System.Windows.Forms.ComboBox>控制項會出現在兩個部分： 上半部是文字方塊，可讓使用者輸入的清單項目。 第二個部分是清單方塊，其中會顯示，使用者可以從中選取一個項目清單。 如需其他樣式下拉式方塊的詳細資訊，請參閱 <<c0> [ 何時使用 Windows Form ComboBox Instead of ListBox](../../../../docs/framework/winforms/controls/when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)。  
  
 <xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>屬性會傳回整數值，對應至選取的清單項目。 您可以變更，以程式設計方式變更選取的項目<xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>程式碼中的值; 在清單中對應的項目會出現在下拉式方塊的文字方塊部分。 如果未不選取任何項目，則<xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>值為-1。 如果選取清單中的第一個項目，則<xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>值為 0。 <xref:System.Windows.Forms.ComboBox.SelectedItem%2A>屬性是類似於<xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>，但傳回的項目本身，通常是字串值。 <xref:System.Windows.Forms.ComboBox.ObjectCollection.Count%2A>屬性會反映在清單中的項目數，而<xref:System.Windows.Forms.ComboBox.ObjectCollection.Count%2A>屬性一律為一個以上的最大的可能<xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>值，因為<xref:System.Windows.Forms.ComboBox.SelectedIndex%2A>以零為起始。  
  
 若要加入或刪除中的項目<xref:System.Windows.Forms.ComboBox>控制，請使用<xref:System.Windows.Forms.ComboBox.ObjectCollection.Add%2A>， <xref:System.Windows.Forms.ComboBox.ObjectCollection.Insert%2A>，<xref:System.Windows.Forms.ComboBox.ObjectCollection.Clear%2A>或<xref:System.Windows.Forms.ComboBox.ObjectCollection.Remove%2A>方法。 或者，您可以將項目加入清單使用<xref:System.Windows.Forms.ComboBox.Items%2A>設計工具中的屬性。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.ComboBox>
- [ListBox 控制項概觀](../../../../docs/framework/winforms/controls/listbox-control-overview-windows-forms.md)
- [何時使用 Windows Forms ComboBox 取代 ListBox](../../../../docs/framework/winforms/controls/when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)
- [如何：新增和移除項目從 Windows Form 的 ComboBox、 ListBox 或 CheckedListBox 控制項](../../../../docs/framework/winforms/controls/add-and-remove-items-from-a-wf-combobox.md)
- [如何：排序內容的 Windows Forms 的 ComboBox、 ListBox 或 CheckedListBox 控制項](../../../../docs/framework/winforms/controls/sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [如何：存取特定項目中的 Windows Forms 的 ComboBox、 ListBox 或 CheckedListBox 控制項](../../../../docs/framework/winforms/controls/access-specific-items-in-a-wf-combobox-listbox-or-checkedlistbox.md)
- [如何：將 Windows Form ComboBox 或 ListBox 控制項繫結至資料](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-combobox-or-listbox-control-to-data.md)
- [用來列出選項的 Windows Forms 控制項](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
- [如何：Windows form 的 ComboBox、 ListBox 或 CheckedListBox 控制項建立查閱資料表](../../../../docs/framework/winforms/controls/create-a-lookup-table-for-a-wf-combobox-listbox.md)
