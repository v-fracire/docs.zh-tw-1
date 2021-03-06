---
title: HOW TO：若要新增或移除集合中的控制項在執行階段
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- run time [Windows Forms], removing controls
- controls [Windows Forms], adding using collections
- controls collections
- collections [Windows Forms], adding items
- run time [Windows Forms], adding controls
- controls [Windows Forms], removing using collections
ms.assetid: 771bf895-3d5f-469b-a324-3528f343657e
ms.openlocfilehash: 88a743cc6d0a1e90d2912c9ec610fae326ff5770
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744904"
---
# <a name="how-to-add-to-or-remove-from-a-collection-of-controls-at-run-time"></a>HOW TO：若要新增或移除集合中的控制項在執行階段
在應用程式開發的一般工作會將控制項加入和移除您的表單上的任何容器控制項的控制項 (例如<xref:System.Windows.Forms.Panel>或<xref:System.Windows.Forms.GroupBox>控制項或甚至是表單本身)。 在設計階段，可以將控制項直接拖曳至面板或群組方塊。 在執行階段，這些控制項會維護 `Controls` 集合，以便持續追蹤有哪些控制項置於其上。  
  
> [!NOTE]
>  下列程式碼範例適用於任何可維護內含控制項集合的控制項。  
  
### <a name="to-add-a-control-to-a-collection-programmatically"></a>以程式設計方式將控制項新增至集合  
  
1.  建立要新增之控制項的執行個體。  
  
2.  設定新控制項的屬性。  
  
3.  將控制項新增至父控制項的 `Controls` 集合。  
  
     下列程式碼範例示範如何建立的執行個體<xref:System.Windows.Forms.Button>控制項。 它需要表單<xref:System.Windows.Forms.Panel>控制項，建立按鈕的事件處理方法， `NewPanelButton_Click`，已經存在。  
  
    ```vb  
    Public NewPanelButton As New Button()  
  
    Public Sub AddNewControl()  
       ' The Add method will accept as a parameter any object that derives  
       ' from the Control class. In this case, it is a Button control.  
       Panel1.Controls.Add(NewPanelButton)  
       ' The event handler indicated for the Click event in the code   
       ' below is used as an example. Substite the appropriate event  
       ' handler for your application.  
       AddHandler NewPanelButton.Click, AddressOf NewPanelButton_Click  
    End Sub  
    ```  
  
    ```csharp  
    public Button newPanelButton = new Button();  
  
    public void addNewControl()  
    {   
       // The Add method will accept as a parameter any object that derives  
       // from the Control class. In this case, it is a Button control.  
       panel1.Controls.Add(newPanelButton);  
       // The event handler indicated for the Click event in the code   
       // below is used as an example. Substitute the appropriate event  
       // handler for your application.  
       this.newPanelButton.Click += new System.EventHandler(this. NewPanelButton_Click);  
    }  
    ```  
  
### <a name="to-remove-controls-from-a-collection-programmatically"></a>以程式設計方式移除集合中的控制項  
  
1.  移除事件的事件處理常式。 在 Visual Basic 中使用[RemoveHandler 陳述式](~/docs/visual-basic/language-reference/statements/removehandler-statement.md)關鍵字，在視覺效果C#，使用[-= 運算子 (C#參考)](~/docs/csharp/language-reference/operators/subtraction-assignment-operator.md)。  
  
2.  使用 `Remove` 方法，從面板的 `Controls` 集合中刪除所需控制項。  
  
3.  呼叫<xref:System.Windows.Forms.Control.Dispose%2A>方法，以釋放控制項所使用的所有資源。  
  
    ```vb  
    Public Sub RemoveControl()  
    ' NOTE: The code below uses the instance of   
    ' the button (NewPanelButton) from the previous example.  
       If Panel1.Controls.Contains(NewPanelButton) Then  
          RemoveHandler NewPanelButton.Click, AddressOf _   
             NewPanelButton_Click  
          Panel1.Controls.Remove(NewPanelButton)  
          NewPanelButton.Dispose()  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void removeControl(object sender, System.EventArgs e)  
    {  
    // NOTE: The code below uses the instance of   
    // the button (newPanelButton) from the previous example.  
       if(panel1.Controls.Contains(newPanelButton))  
       {  
          this.newPanelButton.Click -= new System.EventHandler(this.   
             NewPanelButton_Click);  
          panel1.Controls.Remove(newPanelButton);  
          newPanelButton.Dispose();  
       }  
    }  
    ```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.Panel>
- [Panel 控制項](../../../../docs/framework/winforms/controls/panel-control-windows-forms.md)
