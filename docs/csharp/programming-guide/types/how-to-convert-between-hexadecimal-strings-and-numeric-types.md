---
title: HOW TO：在十六進位字串和數字型別間轉換 - C# 程式設計指南
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- hexadecimal strings [C#], converting to numeric type
- conversions [C#], hexidecimal strings
- strings [C#], converting hexadecimal strings
- hexadecimal strings [C#]
ms.assetid: 7115c49f-7d1d-40c3-8bd9-aae0cc1d46b6
ms.openlocfilehash: 1d6884dc7376c07d2cc6fc03aa3972fb68d39ead
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54615230"
---
# <a name="how-to-convert-between-hexadecimal-strings-and-numeric-types-c-programming-guide"></a>HOW TO：在十六進位字串和數字型別間轉換 (C# 程式設計指南)
這些範例示範如何執行下列工作：  
  
-   取得[字串](../../../csharp/language-reference/keywords/string.md)中每個字元的十六進位值。  
  
-   取十六進位字串中對應每個值的 [char](../../../csharp/language-reference/keywords/char.md)。  
  
-   將十六進位 `string` 轉換成 [int](../../../csharp/language-reference/keywords/int.md)。  
  
-   將十六進位 `string` 轉換成 [float](../../../csharp/language-reference/keywords/float.md)。  
  
-   將 [byte](../../../csharp/language-reference/keywords/byte.md) 陣列轉換成十六進位 `string`。  
  
## <a name="example"></a>範例  
 本例以 `string` 輸出每個字元的十六進位值。 它會先將 `string` 剖析成字元陣列。 接著在每個字元上呼叫 <xref:System.Convert.ToInt32%28System.Char%29>，以取得其數值。 最後，在 `string` 中將數字格式化為十六進位表示法。  
  
 [!code-csharp[csProgGuideTypes#30](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_1.cs)]  
  
## <a name="example"></a>範例  
 本例會剖析十六進位值的 `string`，並輸出對應至每個十六進位值的字元。 它會先呼叫 [Split(Char\[\])](xref:System.String.Split(System.Char[])) 方法，取得每個十六進位值，作為陣列中的個別 `string`。 接著呼叫 <xref:System.Convert.ToInt32%28System.String%2CSystem.Int32%29>，以將十六進位值轉換為呈現為 [int](../../../csharp/language-reference/keywords/int.md) 的十進位值。它會顯示兩種不同取得對應該字元程式碼字元的方式。 第一個技巧使用 <xref:System.Char.ConvertFromUtf32%28System.Int32%29>，傳回對應於整數引數作為 `string` 的字元。 第二個技巧將 `int` 明確轉換成 [char](../../../csharp/language-reference/keywords/char.md)。  
  
 [!code-csharp[csProgGuideTypes#31](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_2.cs)]  
  
## <a name="example"></a>範例  
 這個範例示範另一種將十六進位 `string` 轉換為整數的方式，方法是呼叫 <xref:System.Int32.Parse%28System.String%2CSystem.Globalization.NumberStyles%29> 方法。  
  
 [!code-csharp[csProgGuideTypes#32](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_3.cs)]  
  
## <a name="example"></a>範例  
 下列範例示範如何使用 <xref:System.BitConverter?displayProperty=nameWithType> 類別和 <xref:System.UInt32.Parse%2A?displayProperty=nameWithType> 方法，以將十六進位 `string` 轉換為 [float](../../../csharp/language-reference/keywords/float.md)。  
  
 [!code-csharp[csProgGuideTypes#39](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_4.cs)]  
  
## <a name="example"></a>範例  
 下例示範如何使用 <xref:System.BitConverter?displayProperty=nameWithType> 類別，將 [byte](../../../csharp/language-reference/keywords/byte.md) 陣列轉換為十六進位的字串。  
  
 [!code-csharp[csProgGuideTypes#38](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-convert-between-hexadecimal-strings-and-numeric-types_5.cs)]  
  
## <a name="see-also"></a>另請參閱

- [Standard Numeric Format Strings](../../../standard/base-types/standard-numeric-format-strings.md)
- [型別](../../../csharp/programming-guide/types/index.md)
- [如何：判斷字串是否代表數值](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)
