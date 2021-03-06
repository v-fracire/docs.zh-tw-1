---
title: HOW TO：一次一行讀取文字檔 (Visual C#)
ms.date: 07/20/2015
helpviewer_keywords:
- ReadLine method [C#]
- reading text files, line by line
- text files [C#]
ms.assetid: d62e22c5-a13c-48db-af9b-f10c801b0cb1
ms.openlocfilehash: 831f306a19d926b70170c1a6ebc4ab670f1b9851
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718646"
---
# <a name="how-to-read-a-text-file-one-line-at-a-time-visual-c"></a>HOW TO：一次一行讀取文字檔 (Visual C#)
此範例會使用 `StreamReader` 類別的 `ReadLine` 方法，將文字檔的內容一次一行讀入字串中。 每個文字行都會儲存到字串 `line` 中並顯示在畫面上。  
  
## <a name="example"></a>範例  
  
```csharp
int counter = 0;  
string line;  
  
// Read the file and display it line by line.  
System.IO.StreamReader file =   
    new System.IO.StreamReader(@"c:\test.txt");  
while((line = file.ReadLine()) != null)  
{  
    System.Console.WriteLine(line);  
    counter++;  
}  
  
file.Close();  
System.Console.WriteLine("There were {0} lines.", counter);  
// Suspend the screen.  
System.Console.ReadLine();  
```  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 將程式碼複製並貼到主控台應用程式的 `Main` 方法中。  
  
 以實際檔案名稱取代 `"c:\test.txt"`。  
  
## <a name="robust-programming"></a>穩固程式設計  
 以下條件可能會造成例外狀況：  
  
-   檔案可能不存在。  
  
## <a name="net-framework-security"></a>.NET Framework 安全性  
 請勿根據檔案名稱來判斷檔案內容。 例如，`myFile.cs` 檔案可能不是 C# 原始程式檔。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.IO?displayProperty=nameWithType>
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)
- [檔案系統和登錄 (C# 程式設計指南)](../../../csharp/programming-guide/file-system/index.md)
