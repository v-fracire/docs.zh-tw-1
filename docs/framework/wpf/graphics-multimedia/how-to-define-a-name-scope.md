---
title: HOW TO：定義名稱範圍
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- name scope [WPF], defining
- Storyboards [WPF], animating in procedural code
- animation [WPF], Storyboards [WPF], in procedural code
ms.assetid: 4f361925-6a08-40dc-8231-a61111c6b28b
ms.openlocfilehash: 656c1e9af11697cd4a1253bdab673887765976a6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674462"
---
# <a name="how-to-define-a-name-scope"></a>HOW TO：定義名稱範圍
若要以動畫顯示<xref:System.Windows.Media.Animation.Storyboard>程式碼中，您必須建立<xref:System.Windows.NameScope>並向擁有該名稱範圍的項目中的目標物件的名稱。 在下列範例中，<xref:System.Windows.NameScope>已經為`myMainPanel`。 兩個按鈕`button1`和`button2`，會新增至面板，並註冊其名稱。 數個動畫和<xref:System.Windows.Media.Animation.Storyboard>所建立。 分鏡腳本的<xref:System.Windows.Media.Animation.Storyboard.Begin%2A>方法用來啟動動畫。  
  
 因為`button1`， `button2`，並`myMainPanel`所有共用相同的名稱範圍，其中任何一個可以搭配<xref:System.Windows.Media.Animation.Storyboard><xref:System.Windows.Media.Animation.Storyboard.Begin%2A>方法來啟動動畫。  
  
## <a name="example"></a>範例  
 [!code-csharp[StoryboardBeginAnimation_procedural_snip#NameScopeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/CSharp/ScopeExample.cs#namescopeexample)]
 [!code-vb[StoryboardBeginAnimation_procedural_snip#NameScopeExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/visualbasic/scopeexample.vb#namescopeexample)]  
  
## <a name="see-also"></a>另請參閱
- [使用分鏡腳本建立屬性的動畫](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-by-using-a-storyboard.md)
- [動畫概觀](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
