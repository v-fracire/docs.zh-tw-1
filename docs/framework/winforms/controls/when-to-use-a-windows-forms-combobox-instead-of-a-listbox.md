---
title: 何時使用 Windows Form ComboBox 取代 ListBox
ms.date: 03/30/2017
helpviewer_keywords:
- ListBox control [Windows Forms], adding and removing items
- ListBox control [Windows Forms], vs. ComboBox
- bound controls [Windows Forms], combo boxes
- Windows Forms controls, data binding
- ComboBox control [Windows Forms], compared to ListBox
- combo boxes [Windows Forms], compared to list boxes
- ListBox control [Windows Forms], accessing items
- ListCount property
ms.assetid: 7bcaea58-1cfa-46db-9baf-b75a69d8f9ec
ms.openlocfilehash: e6cdc7f0d54d54448a7b9ed42603b07c93eba719
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668336"
---
# <a name="when-to-use-a-windows-forms-combobox-instead-of-a-listbox"></a>何時使用 Windows Form ComboBox 取代 ListBox
<xref:System.Windows.Forms.ComboBox>而<xref:System.Windows.Forms.ListBox>控制項具有類似的行為，和在某些情況下可能可以互換。 有些的時候，不過，當其中一種是一項工作更適合。  
  
 一般而言，下拉式方塊時，適當沒有建議的選項清單和清單方塊適合，當您想要限制清單上的輸入。 下拉式方塊中將包含文字方塊欄位，因此可以在輸入不在清單上的選項。 例外狀況時，<xref:System.Windows.Forms.ComboBox.DropDownStyle%2A>屬性設定為<xref:System.Windows.Forms.ComboBoxStyle.DropDownList>。 在此情況下，控制項就會選取項目，如果您輸入其第一個字母。  
  
 此外，下拉式方塊會節省空間，在表單上。 因為未顯示的完整清單，直到使用者按一下向下箭號，下拉式方塊可以輕鬆地納入小空間，清單方塊會符合。 例外狀況時，<xref:System.Windows.Forms.ComboBox.DropDownStyle%2A>屬性設定為<xref:System.Windows.Forms.ComboBoxStyle.Simple>： 會顯示完整的清單，並佔用更多的空間比清單方塊的下拉式方塊。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- [如何：新增和移除項目從 Windows Form 的 ComboBox、 ListBox 或 CheckedListBox 控制項](../../../../docs/framework/winforms/controls/add-and-remove-items-from-a-wf-combobox.md)
- [如何：排序內容的 Windows Forms 的 ComboBox、 ListBox 或 CheckedListBox 控制項](../../../../docs/framework/winforms/controls/sort-the-contents-of-a-wf-combobox-listbox-or-checkedlistbox-control.md)
- [用來列出選項的 Windows Forms 控制項](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
