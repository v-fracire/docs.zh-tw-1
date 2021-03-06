---
title: 篩選資料 (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 7749519a-7edc-49fe-aef9-6a353864af6c
ms.openlocfilehash: d65b9941ceffa7ea23c4ead192ec6b97b7b4ead8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527831"
---
# <a name="filtering-data-visual-basic"></a>篩選資料 (Visual Basic)
篩選指的是將結果集限制為只包含符合指定條件之元素的作業， 也稱為選取。  
  
 下圖顯示字元序列的篩選結果。 篩選作業的述詞指定字元必須為 'A'。  
  
 ![LINQ 篩選作業](../../../../csharp/programming-guide/concepts/linq/media/linq_filter.png "LINQ_Filter")  
  
 執行選取的標準查詢運算子方法詳列於下一節。  
  
## <a name="methods"></a>方法  
  
|方法名稱|描述|Visual Basic 查詢運算式語法|更多資訊|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|OfType|根據可轉換為所指定類型的能力來選取值。|不適用。|<xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.OfType%2A?displayProperty=nameWithType>|  
|位置|根據述詞函式來選取值。|`Where`|<xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Where%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a>查詢運算式語法範例  
 下列範例會使用`Where`若要從陣列篩選具有特定長度的字串。  
  
```vb  
Dim words() As String = {"the", "quick", "brown", "fox", "jumps"}  
  
Dim query = From word In words   
            Where word.Length = 3   
            Select word  
  
Dim sb As New System.Text.StringBuilder()  
For Each str As String In query  
    sb.AppendLine(str)  
Next  
  
' Display the results.  
MsgBox(sb.ToString())  
  
' This code produces the following output:  
  
' the  
' fox  
```  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Linq>
- [標準查詢運算子概觀 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Where 子句](../../../../visual-basic/language-reference/queries/where-clause.md)
- [如何：篩選查詢結果](../../../../visual-basic/programming-guide/language-features/linq/how-to-filter-query-results-by-using-linq.md)
- [如何：查詢組件的中繼資料，使用反映 (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-an-assembly-s-metadata-with-reflection-linq.md)
- [如何：查詢具有指定之屬性或名稱 (Visual Basic) 的檔案](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-for-files-with-a-specified-attribute-or-name.md)
- [如何：排序或篩選文字資料，依任何字或欄位 (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-sort-or-filter-text-data-by-any-word-or-field-linq.md)
