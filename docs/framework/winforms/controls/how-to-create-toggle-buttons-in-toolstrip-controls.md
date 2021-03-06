---
title: HOW TO：在 ToolStrip 控制項中建立切換按鈕
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toggle buttons [Windows Forms], creating
- examples [Windows Forms], toolbars
- ToolStrip control [Windows Forms], creating toggle buttons
ms.assetid: d9c197df-4c65-43f2-beee-b68b52b2befc
ms.openlocfilehash: 723916eb0c1e242df301c49bf0716e0262a3ba42
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614974"
---
# <a name="how-to-create-toggle-buttons-in-toolstrip-controls"></a>HOW TO：在 ToolStrip 控制項中建立切換按鈕
當使用者按一下切換按鈕時，它會出現下凹的連線，並保留下凹的外觀，直到使用者按一下按鈕時一次。  
  
### <a name="to-create-a-toggling-toolstripbutton"></a>若要建立切換 prvek ToolStripButton  
  
-   使用程式碼，如下列程式碼範例。 此程式碼假設您的表單包含<xref:System.Windows.Forms.ToolStrip>控制項，且其<xref:System.Windows.Forms.ToolStrip.Items%2A>集合包含<xref:System.Windows.Forms.ToolStripButton>稱為`toolStripButton1`。 同時也假設您已經呼叫事件處理常式`toolStripButton1_CheckedChanged`。  
  
    ```vb  
    toolStripButton1.CheckOnClick = True  
    toolStripButton1.CheckedChanged AddressOf _  
    EventHandler(toolStripButton1_CheckedChanged);  
    ```  
  
    ```csharp  
    toolStripButton1.CheckOnClick = true;  
    toolStripButton1.CheckedChanged += new _  
    EventHandler(toolStripButton1_CheckedChanged);  
    ```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.ToolStripButton>
- [ToolStrip 控制項概觀](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
