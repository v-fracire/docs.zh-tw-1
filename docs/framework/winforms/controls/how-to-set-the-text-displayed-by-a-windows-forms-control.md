---
title: HOW TO：設定所顯示之文字的 Windows Form 控制項
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, captions
- Button control [Windows Forms], button text
- StdFont object and CommandButton caption
- captions [Windows Forms], Windows Forms controls
- Text property [Windows Forms], Windows Forms control
- Button control [Windows Forms], text display
- labels [Windows Forms], adding to CommandButton control
- buttons [Windows Forms], text
- captions [Windows Forms], setting
- text
- examples [Windows Forms], controls
- text [Windows Forms], Windows Forms controls
- controls [Windows Forms], captions
- forms [Windows Forms], captions
ms.assetid: 36b95bff-8780-479d-b86a-f1a0673653aa
ms.openlocfilehash: 30cf71aa2a87ff99ccb965844b620ef08a20b69c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54636440"
---
# <a name="how-to-set-the-text-displayed-by-a-windows-forms-control"></a>HOW TO：設定所顯示之文字的 Windows Form 控制項
Windows Form 控制項通常會顯示與控制項主要功能相關的一些文字。 例如，<xref:System.Windows.Forms.Button> 控制項通常會顯示一個標題，指出當按下按鈕時，就會執行什麼動作。 針對所有控制項，您都可以使用 <xref:System.Windows.Forms.Control.Text%2A> 屬性來設定或傳回該文字。 您可以使用 <xref:System.Windows.Forms.Control.Font%2A> 屬性來變更字型。 您也可以使用設計工具來設定文字。  另請參閱[How to:建立 Windows form 控制項使用設計工具的便捷鍵](how-to-create-access-keys-for-windows-forms-controls-using-the-designer.md)， [How to:設定所顯示之文字的 Windows Form 控制項使用設計工具](how-to-set-the-text-displayed-by-a-windows-forms-control-using-the-designer.md)， [How to:設定所顯示的映像的 Windows Form 控制項使用設計工具](how-to-set-the-image-displayed-by-a-windows-forms-control-using-the-designer.md)。  
  
### <a name="to-set-the-text-displayed-by-a-control-programmatically"></a>以程式設計方式來設定控制項所顯示的文字  
  
1.  將 <xref:System.Windows.Forms.Control.Text%2A> 屬性設為字串。  
  
     若要建立加上底線的便捷鍵，請在要成為便捷鍵的字母前面加上連字號 (&) 字元。  
  
2.  將 <xref:System.Windows.Forms.Control.Font%2A> 屬性設為 <xref:System.Drawing.Font> 類型的物件。  
  
    ```vb  
    Button1.Text = "Click here to save changes"  
    Button1.Font = New Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point)  
    ```  
  
    ```csharp  
    button1.Text = "Click here to save changes";  
    button1.Font = new Font("Arial", 10, FontStyle.Bold,  
       GraphicsUnit.Point);  
    ```  
  
    ```cpp  
    button1->Text = "Click here to save changes";  
    button1->Font = new System::Drawing::Font("Arial",  
       10, FontStyle::Bold, GraphicsUnit::Point);  
    ```  
  
    > [!NOTE]
    >  您可以在使用者介面項目中使用逸出字元來顯示特殊字元，這些使用者介面項目 (例如功能表項目) 通常會以不同方式來解譯該字元。 例如，下列程式碼字行會設定功能表項目的文字來讀取 "& Now For Something Completely Different"：  
  
    ```vb  
    MPMenuItem.Text = "&& Now For Something Completely Different"  
    ```  
  
    ```csharp  
    mpMenuItem.Text = "&& Now For Something Completely Different";  
    ```  
  
    ```cpp  
    mpMenuItem->Text = "&& Now For Something Completely Different";  
    ```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.Control.Text%2A?displayProperty=nameWithType>
- [如何：建立 Windows Form 控制項的便捷鍵](../../../../docs/framework/winforms/controls/how-to-create-access-keys-for-windows-forms-controls.md)
- [如何：回應 Windows Form Button 按一下動作](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)
