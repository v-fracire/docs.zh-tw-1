---
title: HOW TO：定義停駐之 ToolStrip 控制項的疊置順序
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], specifying z-order
- z-order
ms.assetid: 8b595429-ba9f-46af-9c55-3d5cc53f7fff
ms.openlocfilehash: 170aca57a30ca89d8f7a50397ebf61cb1b0b60e4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629624"
---
# <a name="how-to-define-z-ordering-of-docked-toolstrip-controls"></a>HOW TO：定義停駐之 ToolStrip 控制項的疊置順序
若要使用停駐將 <xref:System.Windows.Forms.ToolStrip> 控制項正確地定位，您必須依照表單的疊置順序，將控制項正確地定位。  
  
## <a name="example"></a>範例  
 下列程式碼範例示範如何指定疊置順序，以排列 <xref:System.Windows.Forms.ToolStrip> 控制項和停駐的 <xref:System.Windows.Forms.MenuStrip> 控制項。  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#21](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#21)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#21](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#21)]  
  
 疊置順序取決於順序<xref:System.Windows.Forms.ToolStrip>和 <xref:System.Windows.Forms.MenuStrip>  
  
 控制項會加入至表單的<xref:System.Windows.Forms.Control.Controls%2A>集合。  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#23](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#23)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#23](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#23)]  
  
 將對 <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> 方法的這些呼叫順序反轉，並檢視配置上的效果。  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   System.Design、System.Drawing 和 System.Windows.Forms 組件的參考。  
  
 Visual Basic 或 Visual C# 建置此範例從命令列的相關資訊，請參閱[從命令列建置](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)或是[命令列使用 csc.exe 建置](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)。 您也可以將程式碼貼入新的專案，以建置此範例的 Visual Studio。  另請參閱[How to:編譯並執行完整的 Windows Form 程式碼範例使用 Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.Control.ControlCollection.Add%2A>
- <xref:System.Windows.Forms.Control.Controls%2A>
- <xref:System.Windows.Forms.Control.Dock%2A>
- [ToolStrip 控制項](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
