---
title: HOW TO：載入和顯示中繼檔
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], metafiles
- metafiles [Windows Forms], displaying
ms.assetid: 60af1714-f148-4d85-a739-0557965ffa73
ms.openlocfilehash: d0835d7f2c5ffea44f22661a765ab16b1d0130c5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619554"
---
# <a name="how-to-load-and-display-metafiles"></a>HOW TO：載入和顯示中繼檔
<xref:System.Drawing.Imaging.Metafile>類別，繼承自<xref:System.Drawing.Image>類別中，提供記錄、 顯示及檢查向量影像的方法。  
  
## <a name="example"></a>範例  
 若要在螢幕上顯示為向量影像 （中繼檔），您需要<xref:System.Drawing.Imaging.Metafile>物件和<xref:System.Drawing.Graphics>物件。 將檔案 （或資料流） 的名稱傳遞給<xref:System.Drawing.Imaging.Metafile>建構函式。 建立之後<xref:System.Drawing.Imaging.Metafile>物件，傳遞<xref:System.Drawing.Imaging.Metafile>物件<xref:System.Drawing.Graphics.DrawImage%2A>方法<xref:System.Drawing.Graphics>物件。  
  
 此範例會建立<xref:System.Drawing.Imaging.Metafile>EMF （增強型中繼檔） 檔案中的物件，然後繪製在其左上角的映像 （60，10）。  
  
 下圖顯示中繼檔繪製在指定的位置。  
  
 ![映像位置](../../../../docs/framework/winforms/advanced/media/imageposition2.png "imageposition2")  
  
 [!code-csharp[System.Drawing.WorkingWithImages#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.WorkingWithImages#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 上述範例是為了搭配 Windows Form 使用而設計，且其需要 <xref:System.Windows.Forms.PaintEventArgs> `e`，這是 <xref:System.Windows.Forms.Control.Paint> 事件處理常式的參數。  
  
## <a name="see-also"></a>另請參閱
- [使用影像、點陣圖、圖示和中繼檔](../../../../docs/framework/winforms/advanced/working-with-images-bitmaps-icons-and-metafiles.md)
