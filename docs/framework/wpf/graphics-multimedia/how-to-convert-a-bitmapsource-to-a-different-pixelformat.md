---
title: HOW TO：將 BitmapSource 轉換成不同的 PixelFormat
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BitmapSource objects [WPF], converting to indexed pixel format
- converting images [WPF]
- converting [WPF], BitmapSource objects to indexed pixel formats
- converting [WPF], BitmapSource objects to palettized pixel format
- BitmapSource objects [WPF], converting to palettized pixel format
ms.assetid: cd9df1e4-d5dc-4f57-b67b-4ec67e086b33
ms.openlocfilehash: 572c2bbf1e84160cbce398a349cfb299cee0948d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491398"
---
# <a name="how-to-convert-a-bitmapsource-to-a-different-pixelformat"></a>HOW TO：將 BitmapSource 轉換成不同的 PixelFormat
此範例示範如何將轉換<xref:System.Windows.Media.Imaging.BitmapSource>物件 (<xref:System.Windows.Media.Imaging.BitmapImage>) 到不同<xref:System.Windows.Media.PixelFormat>使用<xref:System.Windows.Media.Imaging.FormatConvertedBitmap>。  
  
## <a name="example"></a>範例  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#PixelFormatConversion](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/PixelFormatsExample.cs#pixelformatconversion)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#PixelFormatConversion](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/PixelFormatsExample.vb#pixelformatconversion)]  
  
## <a name="see-also"></a>另請參閱
- [影像處理概觀](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
