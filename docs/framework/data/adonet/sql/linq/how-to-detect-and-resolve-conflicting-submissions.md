---
title: HOW TO：偵測和解決衝突的提交內容
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 91e27206-01fb-4c7a-8afc-1383a6ac5067
ms.openlocfilehash: ab1b56d409a3b185be15ebc8dc119a57038d55bd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510503"
---
# <a name="how-to-detect-and-resolve-conflicting-submissions"></a>HOW TO：偵測和解決衝突的提交內容
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 提供了許多資源，以便偵測和解決多位使用者變更資料庫所造成的衝突。 如需詳細資訊，請參閱[＜How to：管理變更衝突](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)。  
  
## <a name="example"></a>範例  
 下列範例所示`try` / `catch`區塊，會攔截<xref:System.Data.Linq.ChangeConflictException>例外狀況。 主控台視窗中會顯示每個衝突的實體和成員資訊。  
  
> [!NOTE]
>  您必須納入 `using System.Reflection` 指示詞 (在 Visual Basic 中為 `Imports System.Reflection`)，才能支援資訊擷取。 如需詳細資訊，請參閱<xref:System.Reflection>。  
  
 [!code-csharp[DLinqSubmittingChanges#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#2)]
 [!code-vb[DLinqSubmittingChanges#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#2)]  
  
## <a name="see-also"></a>另請參閱
- [變更和提交資料](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
- [如何：管理變更衝突](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
