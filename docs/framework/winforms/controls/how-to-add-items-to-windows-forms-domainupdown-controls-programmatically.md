---
title: HOW TO：以程式設計方式將項目加入 Windows Form DomainUpDown 控制項
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- spin button control [Windows Forms], adding items
- DomainUpDown control [Windows Forms], adding items to
ms.assetid: fd31d314-33eb-4181-90f8-d32ed0c4e072
ms.openlocfilehash: 865f569da561ec5883b0a0f08fcedb34fc84820c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738556"
---
# <a name="how-to-add-items-to-windows-forms-domainupdown-controls-programmatically"></a>HOW TO：以程式設計方式將項目加入 Windows Form DomainUpDown 控制項
您可以加入 Windows Form 中的項目<xref:System.Windows.Forms.DomainUpDown>在程式碼中的控制項。 呼叫<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A>或是<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A>方法<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection>類別，以將項目加入至控制項的<xref:System.Windows.Forms.DomainUpDown.Items%2A>屬性。 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A>方法會將項目加入至集合中的結尾時<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A>方法會將項目加入指定的位置。  
  
### <a name="to-add-a-new-item"></a>若要加入新項目  
  
1.  使用<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A>方法將項目加入至項目清單的結尾。  
  
    ```vb  
    DomainUpDown1.Items.Add("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Add("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Add("noodles");  
    ```  
  
     -或-  
  
2.  使用<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Insert%2A>方法，以將項目插入位於指定位置的清單。  
  
    ```vb  
    ' Inserts an item at the third position in the list  
    DomainUpDown1.Items.Insert(2, "rice")  
    ```  
  
    ```csharp  
    // Inserts an item at the third position in the list  
    domainUpDown1.Items.Insert(2, "rice");  
    ```  
  
    ```cpp  
    // Inserts an item at the third position in the list  
    domainUpDown1->Items->Insert(2, "rice");  
    ```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.DomainUpDown>
- <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Add%2A?displayProperty=nameWithType>
- <xref:System.Collections.ArrayList.Insert%2A?displayProperty=nameWithType>
- [DomainUpDown 控制項](../../../../docs/framework/winforms/controls/domainupdown-control-windows-forms.md)
- [DomainUpDown 控制項概觀](../../../../docs/framework/winforms/controls/domainupdown-control-overview-windows-forms.md)
