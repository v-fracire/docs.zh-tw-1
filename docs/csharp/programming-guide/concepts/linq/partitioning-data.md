---
title: 分割資料 (C#)
ms.date: 07/20/2015
ms.assetid: 2a5c507b-fe22-443c-a768-dec7f9ec568d
ms.openlocfilehash: 184d9d34e087a06ca3fad9b0a8dad571253b225d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702362"
---
# <a name="partitioning-data-c"></a>分割資料 (C#)
LINQ 中的分割是指將輸入序列分成兩個區段的作業，不用重新排列項目，然後傳回其中一個區段。  
  
 下圖顯示字元序列三種不同分割作業的結果。 第一項作業會傳回序列中的前三個項目。 第二項作業會略過前三個項目，傳回其餘項目。 第三個作業會略過序列中的前兩個項目，傳回接下來的三個元項目。  
  
 ![LINQ 分割作業](../../../../csharp/programming-guide/concepts/linq/media/linq_partition.png "LINQ_Partition")  
  
 分割序列的標準查詢運算子方法詳列於下一節。  
  
## <a name="operators"></a>運算子  
  
|運算子名稱|說明|C# 查詢運算式語法|更多資訊|  
|-------------------|-----------------|---------------------------------|----------------------|  
|Skip|略過項目直至序列中指定的位置為止。|不適用。|<xref:System.Linq.Enumerable.Skip%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Skip%2A?displayProperty=nameWithType>|  
|SkipWhile|根據述詞函式跳過項目，直到不符合條件的項目為止。|不適用。|<xref:System.Linq.Enumerable.SkipWhile%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.SkipWhile%2A?displayProperty=nameWithType>|  
|Take|採用序列中最多到指定位置為止的項目。|不適用。|<xref:System.Linq.Enumerable.Take%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Take%2A?displayProperty=nameWithType>|  
|TakeWhile|根據述詞函式採用項目，直到不符合條件的項目為止。|不適用。|<xref:System.Linq.Enumerable.TakeWhile%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.TakeWhile%2A?displayProperty=nameWithType>|  
  
## <a name="see-also"></a>另請參閱

- <xref:System.Linq>
- [標準查詢運算子概觀 (C#)](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
