---
title: AutoSize 在 TableLayoutPanel 控制項中的行為
ms.date: 03/30/2017
helpviewer_keywords:
- AutoSize property [Windows Forms], tableLayoutPanel control
- controls [Windows Forms], sizing
- localizing forms
- layout [Windows Forms], AutoSize
- sizing [Windows Forms], automatic
- TableLayoutPanel control [Windows Forms], AutoSize behavior
- automatic sizing
- AutoSizeMode property
ms.assetid: 9233e0c3-2fa6-405e-8701-959479b1250e
ms.openlocfilehash: fdaa34ace1f5322c9296d2520d275fdf3f176048
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515728"
---
# <a name="autosize-behavior-in-the-tablelayoutpanel-control"></a>AutoSize 在 TableLayoutPanel 控制項中的行為
## <a name="distinct-autosize-behaviors"></a>不同的調整行為  
 <xref:System.Windows.Forms.TableLayoutPanel>控制項支援自動調整大小行為如下：  
  
-   透過<xref:System.Windows.Forms.Control.AutoSize%2A>屬性;  
  
-   透過<xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A>屬性上的<xref:System.Windows.Forms.TableLayoutPanel>控制項的資料行和資料列的樣式。  
  
### <a name="the-autosize-property-with-row-and-column-styles"></a>AutoSize 屬性與資料列和資料行樣式  
 下表描述之間的互動<xref:System.Windows.Forms.Control.AutoSize%2A>屬性和<xref:System.Windows.Forms.TableLayoutPanel>控制項的資料行和資料列的樣式。  
  
|自動調整設定|樣式互動|  
|----------------------|-----------------------|  
|`false`|<xref:System.Windows.Forms.TableLayoutPanel>控制會繼續從左到右，和資料行或資料列，或依照下列順序，配置空間。<br /><br /> 1.如果<xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A>屬性設定為<xref:System.Windows.Forms.SizeType.Absolute>，所指定的像素數<xref:System.Windows.Forms.ColumnStyle.Width%2A>或<xref:System.Windows.Forms.RowStyle.Height%2A>配置。<br />2.如果<xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A>屬性設定為<xref:System.Windows.Forms.SizeType.AutoSize>，傳回的子控制項的像素數<xref:System.Windows.Forms.Control.GetPreferredSize%2A>配置方法。<br />3.之後的所有空間<xref:System.Windows.Forms.SizeType.Absolute>並<xref:System.Windows.Forms.SizeType.AutoSize>資料行或資料列配置時，任何資料行或資料列<xref:System.Windows.Forms.TableLayoutStyle.SizeType%2A>設定為<xref:System.Windows.Forms.SizeType.Percent>按比例配置剩餘的可用空間|  
|`true`|類似於先前的互動，發生例外狀況，<xref:System.Windows.Forms.SizeType.Percent>資料行或資料列取得的自動調整大小的一環。<br /><br /> <xref:System.Windows.Forms.TableLayoutPanel>控制展開的資料行或資料列建立足夠的可用空間，讓任何資料行或資料列<xref:System.Windows.Forms.SizeType.Percent>樣式裁剪其內容。 <xref:System.Windows.Forms.TableLayoutPanel>控制配置的新空間按比例根據<xref:System.Windows.Forms.ColumnStyle.Width%2A>或<xref:System.Windows.Forms.RowStyle.Height%2A>屬性。|  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Forms.TableLayoutPanel>
- [TableLayoutPanel 控制項概觀](../../../../docs/framework/winforms/controls/tablelayoutpanel-control-overview.md)
