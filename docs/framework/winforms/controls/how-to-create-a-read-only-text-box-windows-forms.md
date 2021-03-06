---
title: HOW TO：建立唯讀文字方塊 (Windows Form)
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [Windows Forms], read-only
- read-only text boxes
- text boxes [Windows Forms], read-only
ms.assetid: 60baa9ab-fa57-44ad-bb7c-61b05aa64296
ms.openlocfilehash: 89d331f6c7fad5880aff031eb808199292e493a6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670334"
---
# <a name="how-to-create-a-read-only-text-box-windows-forms"></a>HOW TO：建立唯讀文字方塊 (Windows Form)
您可以將可編輯的 Windows Form 文字方塊中轉換成唯讀的控制項。 例如，文字方塊可能會顯示值通常進行編輯，但可能不是目前因為應用程式的狀態。  
  
### <a name="to-create-a-read-only-text-box"></a>若要建立唯讀文字方塊  
  
1.  設定<xref:System.Windows.Forms.TextBox>控制項的<xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A>屬性設`true`。 屬性設為`true`，使用者仍然可以捲動，並反白顯示 不允許變更 文字 方塊中的文字。 A**複製**命令會在文字方塊中中, 運作，但**剪下**並**貼上**命令不是。  
  
    > [!NOTE]
    >  <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A>屬性只會影響在執行階段的使用者互動。 您仍然可以變更文字方塊內容以程式設計方式在執行階段變更<xref:System.Windows.Forms.TextBox.Text%2A>文字方塊的屬性。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.TextBox>
- [TextBox 控制項概觀](../../../../docs/framework/winforms/controls/textbox-control-overview-windows-forms.md)
- [如何：控制 Windows Forms TextBox 控制項中的插入點](../../../../docs/framework/winforms/controls/how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [如何：使用 Windows Forms TextBox 控制項建立密碼文字方塊](../../../../docs/framework/winforms/controls/how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [如何：將引號放入字串](../../../../docs/framework/winforms/controls/how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [如何：在 Windows Forms TextBox 控制項中選取文字](../../../../docs/framework/winforms/controls/how-to-select-text-in-the-windows-forms-textbox-control.md)
- [如何：在 Windows Forms TextBox 控制項中檢視多行](../../../../docs/framework/winforms/controls/how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox 控制項](../../../../docs/framework/winforms/controls/textbox-control-windows-forms.md)
