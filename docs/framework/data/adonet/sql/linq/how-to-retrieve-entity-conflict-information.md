---
title: HOW TO：擷取實體衝突資訊
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9a02b608-e7bb-4041-a452-a7fed26fd008
ms.openlocfilehash: 1c2f9a5f822d8783f997c9c5c09ef508c2d8dca7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629029"
---
# <a name="how-to-retrieve-entity-conflict-information"></a>HOW TO：擷取實體衝突資訊
您可以使用 <xref:System.Data.Linq.ObjectChangeConflict> 類別的物件，提供有關 <xref:System.Data.Linq.ChangeConflictException> 例外狀況所揭露的衝突資訊。 如需詳細資訊，請參閱[開放式並行存取：概觀](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md)。  
  
## <a name="example"></a>範例  
 下列範例會逐一查看累積衝突的清單。  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>另請參閱
- [如何：管理變更衝突](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
