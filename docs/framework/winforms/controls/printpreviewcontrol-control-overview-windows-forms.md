---
title: PrintPreviewControl 控制項概觀 (Windows Form)
ms.date: 03/30/2017
f1_keywords:
- PrintPreviewControl
helpviewer_keywords:
- print preview
- PrintPreviewControl control
ms.assetid: 4513c6c7-5e9b-4f4c-82ca-00f993a26955
ms.openlocfilehash: acf21365d2694cdc1bf2213187fb2ae047205c4c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54665368"
---
# <a name="printpreviewcontrol-control-overview-windows-forms"></a>PrintPreviewControl 控制項概觀 (Windows Form)
Windows Forms<xref:System.Windows.Forms.PrintPreviewControl>用來顯示[PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md)列印時出現。 這個控制項沒有任何按鈕或其他使用者介面項目，因此，通常只有當您想要撰寫您自己的預覽列印使用者介面時，才會使用 <xref:System.Windows.Forms.PrintPreviewControl>。 如果您想要的標準使用者介面，使用<xref:System.Windows.Forms.PrintPreviewDialog>控制，請參閱[PrintPreviewDialog 控制項概觀](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md)的概觀。  
  
## <a name="key-properties"></a>索引鍵內容  
 控制項的索引鍵屬性是<xref:System.Windows.Forms.PrintPreviewControl.Document%2A>，可設定要預覽的文件。 必須是文件<xref:System.Drawing.Printing.PrintDocument>物件。 建立列印的文件的概觀，請參閱[PrintDocument 元件概觀](../../../../docs/framework/winforms/controls/printdocument-component-overview-windows-forms.md)並[Windows Forms 列印支援](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)。 <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A>和<xref:System.Windows.Forms.PrintPreviewControl.Rows%2A>屬性會決定控制項上顯示水平和垂直的頁數。 消除鋸齒功能可以讓文字出現更順暢，但可能也會使速度較慢; 顯示若要使用它，將<xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A>屬性設`true`。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.PrintPreviewControl>
- [PrintPreviewDialog 控制項概觀](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md)
- [PrintPreviewControl 控制項](../../../../docs/framework/winforms/controls/printpreviewcontrol-control-windows-forms.md)
- [對話方塊控制項和元件](../../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md)
