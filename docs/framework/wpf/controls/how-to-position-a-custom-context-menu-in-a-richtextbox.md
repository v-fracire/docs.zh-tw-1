---
title: HOW TO：在 RichTextBox 中放置自訂內容功能表
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom context menus [WPF], positioning
- positioning custom context menus [WPF]
- RichTextBox control [WPF], positioning custom context menus
- context menus [WPF], positioning
ms.assetid: bf77c930-a546-4573-9a56-9af345ba189a
ms.openlocfilehash: 1f6e7255286d065eb26773d524a3147801933406
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54727894"
---
# <a name="how-to-position-a-custom-context-menu-in-a-richtextbox"></a>HOW TO：在 RichTextBox 中放置自訂內容功能表
此範例說明如何放置自訂操作功能表<xref:System.Windows.Controls.RichTextBox>。  
  
 當您實作 **RichTextBox** 的自訂操作功能表時，需負責處理操作功能表的位置。  自訂操作功能表預設會在 **RichTextBox** 的中央開啟。  
  
## <a name="example"></a>範例  
 若要覆寫預設放置行為，請新增 接聽程式<xref:System.Windows.FrameworkContentElement.ContextMenuOpening>事件。  下列範例顯示如何以程式設計方式執行此操作。  
  
 [!code-csharp[RichTextBox_ContextMenu#_AddListener](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_addlistener)]
 [!code-vb[RichTextBox_ContextMenu#_AddListener](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_addlistener)]  
  
## <a name="example"></a>範例  
 下列範例示範實作對應<xref:System.Windows.FrameworkContentElement.ContextMenuOpening>事件接聽程式。  
  
 [!code-csharp[RichTextBox_ContextMenu#_ListenerBody](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_listenerbody)]
 [!code-vb[RichTextBox_ContextMenu#_ListenerBody](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_listenerbody)]  
  
## <a name="see-also"></a>另請參閱
- [RichTextBox 概觀](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
- [TextBox 概觀](../../../../docs/framework/wpf/controls/textbox-overview.md)
