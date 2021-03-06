---
title: HOW TO：指定腳本動畫之間的傳遞行為
ms.date: 03/30/2017
helpviewer_keywords:
- Storyboards [WPF], handoff behavior between animations
- animation [WPF], handoff behavior between
ms.assetid: 97bd6842-929b-49d9-813e-46553ae46472
ms.openlocfilehash: 9a27c377e2993c1e67ada508071698a541cec660
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305437"
---
# <a name="how-to-specify-handoffbehavior-between-storyboard-animations"></a>HOW TO：指定腳本動畫之間的傳遞行為
此範例示範如何指定分鏡腳本動畫之間的遞移式行為。 <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>屬性<xref:System.Windows.Media.Animation.BeginStoryboard>指定新動畫已套用至屬性的任何現有的互動。  
  
## <a name="example"></a>範例  
 下列範例會建立兩個按鈕放大滑鼠游標移到上面時，會變小，當資料指標移開。 如果您將滑鼠移的按鈕，並快速移除資料指標，第一個完成之前，將會套用第二個動畫。 當兩個動畫重疊像這樣，您可以看到之間的差異<xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>的值<xref:System.Windows.Media.Animation.HandoffBehavior.Compose>和<xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace>。 值為<xref:System.Windows.Media.Animation.HandoffBehavior.Compose>結合了重疊造成的值時的動畫之間順暢轉換的動畫<xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace>使新動畫立即取代先前的重疊的動畫。  
  
 [!code-xaml[timingbehaviors_snip#HandoffBehaviorWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/HandoffBehaviorExample.xaml#handoffbehaviorwholepage)]  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Windows.Media.Animation.BeginStoryboard>
- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>
- [動畫概觀](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [動畫和計時](https://msdn.microsoft.com/library/7d83765b-d5ae-41b1-b423-80206e1124aa)
- [動畫和計時 how to 主題](animation-and-timing-how-to-topics.md)
