---
title: 指標比較 - C# 程式設計指南
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], comparison
ms.assetid: fcafd514-7405-4deb-8490-cc58efda5495
ms.openlocfilehash: a2cbbabdad1d79c82bb5b3ec02a391727e552c98
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718633"
---
# <a name="pointer-comparison-c-programming-guide"></a>指標比較 (C# 程式設計手冊)
您可以套用下列運算子來比較任何類型的指標：  
  
 **==   !=   \<   >   \<=   >=**  
  
 比較運算子會比較兩個運算元的位址，就像它們是不帶正負號的整數一樣。  
  
## <a name="example"></a>範例  
 [!code-csharp[csProgGuidePointers#16](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#17](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_2.cs)]  
  
## <a name="sample-output"></a>範例輸出  
 `True`  
  
 `False`  
  
## <a name="see-also"></a>另請參閱

- [C# 程式設計指南](../../../csharp/programming-guide/index.md)
- [指標運算式](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [C# 運算子](../../../csharp/language-reference/operators/index.md)
- [指標操作](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)
- [指標型別](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [型別](../../../csharp/language-reference/keywords/types.md)
- [Unsafe.DangerousAPI](../../../csharp/language-reference/keywords/unsafe.md)
- [fixed 陳述式](../../../csharp/language-reference/keywords/fixed-statement.md)
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
