---
title: HOW TO：設定 MDI 應用程式的自動功能表合併
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- Merging [Windows Forms], automatic menu
ms.assetid: 55e32cad-1141-4a56-aa33-d9543ca3d393
ms.openlocfilehash: 3aeaf9ee4818b6689905c10d2bd46fc887609c35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549820"
---
# <a name="how-to-set-up-automatic-menu-merging-for-mdi-applications"></a>HOW TO：設定 MDI 應用程式的自動功能表合併
下列程序提供的基本步驟來設定在多重文件介面 (MDI) 應用程式中使用的自動合併<xref:System.Windows.Forms.MenuStrip>。  
  
### <a name="to-set-up-automatic-menu-merging"></a>若要設定自動功能表合併功能  
  
1.  建立 MDI 父表單，藉由設定其<xref:System.Windows.Forms.Form.IsMdiContainer%2A>屬性設`true`。  
  
2.  新增<xref:System.Windows.Forms.MenuStrip>到 MDI 父代，設定其<xref:System.Windows.Forms.Form.MainMenuStrip%2A>屬性， <xref:System.Windows.Forms.MenuStrip>。  
  
3.  建立 MDI 子表單，並設定其<xref:System.Windows.Forms.Form.MdiParent%2A>屬性，以父表單的名稱。  
  
4.  新增<xref:System.Windows.Forms.MenuStrip>MDI 子表單。  
  
5.  在 子表單中，設定<xref:System.Windows.Forms.ToolStripItem.Visible%2A>的屬性<xref:System.Windows.Forms.MenuStrip>至`false`。  
  
6.  將功能表項目新增至子表單<xref:System.Windows.Forms.MenuStrip>想要合併至父表單的<xref:System.Windows.Forms.MenuStrip>何時啟動的子表單。  
  
7.  使用<xref:System.Windows.Forms.ToolStripItem.MergeAction%2A>功能表上的屬性項目在子表單的<xref:System.Windows.Forms.MenuStrip>來控制它們合併至父表單的方式。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [MenuStrip 控制項概觀](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
