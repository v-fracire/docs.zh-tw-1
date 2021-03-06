---
title: 如何：調整段落之間的間距
ms.date: 03/30/2017
helpviewer_keywords:
- spacing between paragraphs [WPF]
- paragraphs [WPF], spacing between
- documents [WPF], adjusting spacing between paragraphs
ms.assetid: 7cd2f2ac-0e19-4587-bfb6-7f5b18c9536e
ms.openlocfilehash: b232903054cf45b70ba99a9223352391498cf79b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33542944"
---
# <a name="how-to-adjust-spacing-between-paragraphs"></a>如何：調整段落之間的間距
此範例顯示如何調整或排除段落中非固定格式內容之間的間距。  
  
 在非固定格式內容的段落之間會出現額外空間是這些段落; 上設定的邊界的結果因此，可以控制段落間距調整邊界的段落。  若要完全消除兩個段落的額外間距，設定的邊界的段落**0**。  若要達到整個段落的統一間距<xref:System.Windows.Documents.FlowDocument>，使用樣式設定來設定所有段落中的統一的邊界值<xref:System.Windows.Documents.FlowDocument>。  
  
 請務必注意，兩個相鄰的段落的邊界會 「 摺疊 」 到較大的兩個邊界，而非倍。 因此，如果兩個相鄰的段落分別有 20 像素和 40 像素的邊界，段落產生間距是 40 像素，較大的兩個邊界值。  
  
## <a name="example"></a>範例  
 下列範例會使用樣式將邊界設定所有<xref:System.Windows.Documents.Paragraph>中的項目<xref:System.Windows.Documents.FlowDocument>至**0**，其有效地排除段落中的額外間距<xref:System.Windows.Documents.FlowDocument>。  
  
 [!code-xaml[BlockSnippets#_ParagraphSpacingXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BlockSnippets/CSharp/Window1.xaml#_paragraphspacingxaml)]
