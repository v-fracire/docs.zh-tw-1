---
title: 輸入超過檔案結尾
ms.date: 07/20/2015
f1_keywords:
- vbrID62
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
ms.openlocfilehash: 29a9b5ce3c3f8e6a02b52beda1338fd699143570
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491333"
---
# <a name="input-past-end-of-file"></a>輸入超過檔案結尾
任一`Input`陳述式會讀取檔案是空的還是會使用所有的資料，或您使用`EOF`進行二進位存取中開啟檔案的函式。  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1.  使用`EOF`函式之前立即`Input`陳述式來偵測檔案的結尾。  
  
2.  如果開啟檔案以進行二進位存取，使用`Seek`和`Loc`。  
  
## <a name="see-also"></a>另請參閱
- <xref:Microsoft.VisualBasic.FileSystem.Input%2A>
- <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>
- <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>
