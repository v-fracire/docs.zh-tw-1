---
title: 在 LINQ to Entities 查詢中呼叫函式
ms.date: 03/30/2017
ms.assetid: 12a525a9-727c-4464-a0c7-71a0ef541792
ms.openlocfilehash: 8cb861c72f33a7dff3d6bef94719ae590a13706d
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828146"
---
# <a name="calling-functions-in-linq-to-entities-queries"></a>在 LINQ to Entities 查詢中呼叫函式
本章節的主題描述如何使用呼叫 LINQ to Entities 查詢中的函式。  
  
 <xref:System.Data.Objects.EntityFunctions> 與 <xref:System.Data.Objects.SqlClient.SqlFunctions> 類別可讓您存取標準函式與資料庫函式，這些函式是 Entity Framework 的一部分。 如需詳細資訊，請參閱[＜How to：呼叫標準函式](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md)和[How to:呼叫資料庫函式](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md)。  
  
 呼叫自訂函式的程序需要三個基本步驟：  
  
1.  定義概念模型中的函式或宣告儲存模型中的函式。  
  
2.  使用 <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute> 將方法加入至應用程式，並將它對應至模型中的函式。  
  
3.  呼叫 LINQ to Entities 查詢中的函式。  
  
 如需詳細資料，請參閱本節中的主題。  
  
## <a name="in-this-section"></a>本節內容  
 [如何：呼叫標準函式](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md)  
  
 [如何：呼叫資料庫函式](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md)  
  
 [如何：呼叫自訂資料庫函式](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-custom-database-functions.md)  
  
 [如何：在查詢中呼叫模型定義函式](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-in-queries.md)  
  
 [如何：呼叫模型定義函式當做物件方法](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-as-object-methods.md)  
  
## <a name="see-also"></a>另請參閱
- [LINQ to Entities 中的查詢](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
- [標準函式](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
- [.edmx 檔案概觀](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))
- [如何：概念模型中定義自訂函式](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456812(v=vs.100))
