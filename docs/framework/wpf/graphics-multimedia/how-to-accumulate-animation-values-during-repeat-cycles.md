---
title: HOW TO：在重複循環期間累加動畫值
ms.date: 03/30/2017
helpviewer_keywords:
- accumulating animation values across repeating cycles [WPF]
- animation [WPF], accumulating values across repeating cycles
ms.assetid: 548df369-c7cc-4dab-b569-08b95ced2e7e
ms.openlocfilehash: 6e98b7eefd0c30e728b60926096c0f082bc079ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587277"
---
# <a name="how-to-accumulate-animation-values-during-repeat-cycles"></a>HOW TO：在重複循環期間累加動畫值
此範例示範如何使用<xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A>累加動畫值，在重複循環的屬性。  
  
## <a name="example"></a>範例  
 使用<xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A>累積在重複循環的基底值的動畫的屬性。 比方說，如果您將設定重複 9 次的動畫 (<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> = 「 9 倍 」)，並設定要以動畫顯示介於 10 到 15 之間的屬性 (從 = 10 到 = 15)，屬性以動畫顯示從 10 到 15 之間在第一個週期中，從 15 到 20，第二個週期從 20 到 25 期間第三個週期，依此類推。 因此，每個動畫循環會使用從先前的動畫循環結束的動畫值，做為其基底值。  
  
 您可以使用`IsCumulative`具有最基本的動畫和大部分的主要畫面格動畫屬性。 如需詳細資訊，請參閱 <<c0> [ 動畫概觀](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)並[主要畫面格動畫概觀](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)。  
  
 下列範例會示範此行為，以動畫顯示四個矩形的寬度。 範例：  
  
-   以動畫顯示的第一個矩形<xref:System.Windows.Media.Animation.DoubleAnimation>，並設定<xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A>屬性設`true`。  
  
-   以動畫顯示第二個矩形<xref:System.Windows.Media.Animation.DoubleAnimation>，並設定<xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A>屬性的預設值為`false`。  
  
-   以動畫顯示的第三個矩形<xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>，並設定<xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A>屬性設`true`。  
  
-   以動畫顯示最後一個矩形<xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>，並設定<xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A>屬性設`false`。  
  
 [!code-xaml[timingbehaviors_snip#IsCumulativeWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsCumulativeExample.xaml#iscumulativewholepage)]  
  
## <a name="see-also"></a>另請參閱
- [將動畫輸出值加入至動畫啟動值](../../../../docs/framework/wpf/graphics-multimedia/how-to-add-an-animation-output-value-to-an-animation-starting-value.md)
- [重複動畫](../../../../docs/framework/wpf/graphics-multimedia/how-to-repeat-an-animation.md)
- [動畫概觀](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [主要畫面格動畫概觀](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
- [HOW-TO 主題](../../../../docs/framework/wpf/graphics-multimedia/animation-and-timing-how-to-topics.md)
