---
title: SchemaImporterExtension 技術範例
ms.date: 03/30/2017
ms.assetid: 3f5eb78f-0ef6-433a-b095-3a63b1ce0bc9
ms.openlocfilehash: 04e2b3f9fb1ea6f9bbb3c1e1886911cbacda7a62
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54633894"
---
# <a name="schemaimporterextension-technology-sample"></a>SchemaImporterExtension 技術範例
[下載範例](https://download.microsoft.com/download/4/7/B/47B2164C-E780-4B10-8DE4-2CB5B886E0A6/Technologies/Serialization/Xml%20Serialization/SchemaImporterExtension.zip.exe)  
  
 這個範例示範了自訂的 <xref:System.Xml.Serialization.Advanced.SchemaImporterExtension>，它能夠在匯入 XML 結構描述時，精細地控制程式碼的產生。 應用程式中會示範如何建置、註冊及叫用 (Invoke) 這個擴充功能。  
  
### <a name="to-build-the-sample-using-the-command-prompt"></a>若要使用命令提示字元建置範例  
  
1.  開啟 [命令提示字元] 視窗，並巡覽至此範例任一程式設計語言的子目錄。  
  
2.  在命令列鍵入 **msbuild.exe OrderSchemaImporterExtension.sln**。  
  
### <a name="to-build-the-sample-using-visual-studio"></a>若要使用 Visual Studio 建置範例  
  
1.  開啟 [!INCLUDE[fileExplorer](../../../includes/fileexplorer-md.md)]，並巡覽至此範例任一程式設計語言的子目錄。  
  
2.  按兩下 [OrderSchemaImporterExtension.sln] 的圖示，在 Visual Studio 中開啟這個檔案。  
  
3.  在 [ **建置** ] 功能表上，按一下 [ **建置方案**]。  
  
 應用程式便會建置在預設的 \bin 或 \bin\Debug 目錄中。  
  
### <a name="to-run-the-sample"></a>若要執行範例  
  
1.  使用 [命令提示字元]，巡覽至包含新可執行檔的目錄。  
  
2.  在命令列鍵入 **[exe name]**。  
  
## <a name="remarks"></a>備註  
 如需二進位碼建立和註冊步驟之範例的詳細資訊，請參閱原始程式碼和 build.proj 檔案中的註解。  
  
## <a name="see-also"></a>另請參閱

- <xref:System.CodeDom.CodeCompileUnit>
- <xref:System.CodeDom.CodeNamespace>
- <xref:System.CodeDom.CodeNamespaceImport>
- <xref:Microsoft.CSharp.CSharpCodeProvider>
- <xref:System.Xml.Serialization.IXmlSerializable>
- <xref:System.Xml.Serialization.Advanced.SchemaImporterExtension>
- <xref:System.CodeDom>
- <xref:System.CodeDom.Compiler>
- <xref:System.Web.Services.Description>
- <xref:System.Web.Services.Discovery>
- <xref:System.Xml.Serialization>
- <xref:System.Uri>
- <xref:Microsoft.VisualBasic.VBCodeProvider>
- <xref:System.Web.Services.Description.WebReference>
- <xref:System.Xml.Serialization.XmlSchemaImporter>
