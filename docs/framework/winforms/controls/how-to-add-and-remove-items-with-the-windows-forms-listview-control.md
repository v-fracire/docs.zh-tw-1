---
title: HOW TO：新增和移除項目，使用 Windows Forms ListView 控制項
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], populating
- list views [Windows Forms], adding list items
- ListView control [Windows Forms], adding list items
ms.assetid: 1b35a80a-edd8-495f-a807-a28c4aae52c6
ms.openlocfilehash: 7a4083d54ea85ff7a2e18f7e448f2b967317ac25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544519"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control"></a>HOW TO：新增和移除項目，使用 Windows Forms ListView 控制項
加入 Windows Form 中的項目中的程序<xref:System.Windows.Forms.ListView>控制主要包含指定的項目，並將屬性指派給它。 隨時都可以新增或移除清單項目。  
  
### <a name="to-add-items-programmatically"></a>以程式設計方式將項目  
  
1.  使用<xref:System.Windows.Forms.ListView.ListViewItemCollection.Add%2A>方法的<xref:System.Windows.Forms.ListView.Items%2A>屬性。  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#11)]  
  
### <a name="to-remove-items-programmatically"></a>若要以程式設計方式移除項目  
  
1.  使用<xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A>或是<xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A>方法<xref:System.Windows.Forms.ListView.Items%2A>屬性。 <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A>方法會移除單一項目;<xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A>方法從清單中移除所有項目。  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.ListView>
- [ListView 控制項](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)
- [ListView 控制項概觀](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
