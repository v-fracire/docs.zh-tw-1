---
title: 編碼不能設定為 Nothing。
ms.date: 07/20/2015
ms.assetid: 59f7c731-8291-4a85-bf51-c225e48cdc84
ms.openlocfilehash: 99dbd1a068cabca7f57b6d5e8dd13e1069aede65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691319"
---
# <a name="encoding-cannot-be-set-to-nothing"></a>編碼不能設定為 Nothing。
讀取或寫入檔案的嘗試失敗，因為參數 `encoding` 已設定為 `Nothing` ，但需要有效的值。  
  
 <xref:System.Text.Encoding> 用來判斷在寫入檔案時要使用的編碼方式。 預設值為 UTF-8。  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
-   請為 `encoding` 參數提供有效的值。  
  
## <a name="see-also"></a>另請參閱
- [檔案編碼方式](../../visual-basic/developing-apps/programming/drives-directories-files/file-encodings.md)
- [從檔案讀取](../../visual-basic/developing-apps/programming/drives-directories-files/reading-from-files.md)
- [寫入檔案](../../visual-basic/developing-apps/programming/drives-directories-files/writing-to-files.md)
- [My.Computer.FileSystem.ReadAllText](xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A)
- [My.Computer.FileSystem.WriteAllText](xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A)
