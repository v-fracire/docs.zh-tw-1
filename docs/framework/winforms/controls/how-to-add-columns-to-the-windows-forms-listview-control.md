---
title: HOW TO：資料行加入 Windows Form ListView 控制項
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], adding column headers
- columns [Windows Forms], adding to ListView controls
- list views [Windows Forms], adding columns
ms.assetid: 79174274-12ee-4a5d-80db-6ec02976d010
ms.openlocfilehash: eed032ec0bacd50666c30979b33362dabf00d565
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700191"
---
# <a name="how-to-add-columns-to-the-windows-forms-listview-control"></a>HOW TO：資料行加入 Windows Form ListView 控制項
在詳細資料檢視中，<xref:System.Windows.Forms.ListView>控制項可以顯示多個資料行的每個清單項目。 若要向使用者顯示數種類型的每個清單項目的相關資訊，您可以使用資料行。 例如，檔案名稱、 檔案類型、 大小和檔案上次修改的日期，可以顯示一份檔案。 如需在建立後，擴展資料行資訊，請參閱[How to:使用 Windows 的資料行顯示子項目 Form ListView 控制項](../../../../docs/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)。  
  
### <a name="to-add-columns-programmatically"></a>以程式設計方式將資料行  
  
1.  將控制項的<xref:System.Windows.Forms.ListView.View%2A>屬性設<xref:System.Windows.Forms.View.Details>。  
  
2.  使用<xref:System.Windows.Forms.ListView.ColumnHeaderCollection.Add%2A>方法的清單檢視的<xref:System.Windows.Forms.ListView.Columns%2A>屬性。  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#31)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.ListView>
- [ListView 控制項](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)
- [ListView 控制項概觀](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
