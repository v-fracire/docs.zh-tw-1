---
title: 傳回兩個序列之間的集合差異
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 62efb546-c898-408f-af21-36e7c6fed217
ms.openlocfilehash: 282ec36a2ad489e77db9fb5b338d3189c3001f03
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54609027"
---
# <a name="return-the-set-difference-between-two-sequences"></a>傳回兩個序列之間的集合差異
使用 <xref:System.Linq.Queryable.Except%2A> 運算子傳回兩個序列之間的集合差異。  
  
## <a name="example"></a>範例  
 這個範例會使用 <xref:System.Linq.Queryable.Except%2A> 傳回有 `Customers` 居住但無 `Employees` 居住的所有國家 (地區) 序列。  
  
 [!code-csharp[DLinqQueryExamples#41](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#41)]
 [!code-vb[DLinqQueryExamples#41](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#41)]  
  
 在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，<xref:System.Linq.Queryable.Except%2A> 作業僅妥善定義於集合上。 尚未定義多重集 (Multiset) 的語意 (Semantics)。  
  
## <a name="see-also"></a>另請參閱
- [查詢範例](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
- [標準查詢運算子轉譯](../../../../../../docs/framework/data/adonet/sql/linq/standard-query-operator-translation.md)
