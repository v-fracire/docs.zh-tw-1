---
title: HOW TO：資料行表示為類別成員
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ab28021-4d15-4d9c-bf2e-6ccc0daa7d1a
ms.openlocfilehash: 7a772de27583f35b18a4fa5854e61768443e5ba5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54652552"
---
# <a name="how-to-represent-columns-as-class-members"></a>HOW TO：資料行表示為類別成員
使用[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<xref:System.Data.Linq.Mapping.ColumnAttribute>欄位或屬性相關聯的資料庫資料行的屬性。  
  
### <a name="to-map-a-field-or-property-to-a-database-column"></a>若要將欄位或屬性 (Property) 對應至資料庫資料行  
  
-   將 <xref:System.Data.Linq.Mapping.ColumnAttribute> 屬性 (Attribute) 加入至屬性 (Property) 或欄位宣告。  
  
## <a name="example"></a>範例  
 下列程式碼會將 `CustomerID` 類別中的 `Customer` 欄位對應至 `CustomerID` 資料庫資料表中的 `Customers` 資料行。  
  
 [!code-csharp[DLinqCustomize#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#2)]
 [!code-vb[DLinqCustomize#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#2)]  
  
 如果可以推斷名稱，您就不必指定 <xref:System.Data.Linq.Mapping.DataAttribute.Name%2A> 屬性。 如果您未指定名稱，則會假設名稱就是與屬性或欄位名稱相同的名稱。  
  
## <a name="see-also"></a>另請參閱
- [LINQ to SQL 物件模型](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [如何：使用程式碼編輯器自訂實體類別](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
