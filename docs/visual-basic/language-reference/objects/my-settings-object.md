---
title: My.Settings 物件 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MySettingsProperty.Settings
- My.Settings
helpviewer_keywords:
- My.Settings object
ms.assetid: 41f30dc1-202a-4273-b9b7-5728941f996c
ms.openlocfilehash: 293e7cd6449b8a35b5e42b4823a4412e0d6a3f14
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628158"
---
# <a name="mysettings-object"></a>My.Settings 物件
提供屬性和方法，以存取應用程式的設定。  
  
## <a name="remarks"></a>備註  
 `My.Settings`物件可讓您存取應用程式的設定，並可讓您以動態方式儲存及擷取屬性設定和應用程式的其他資訊。 如需詳細資訊，請參閱[管理應用程式設定 (.NET)](/visualstudio/ide/managing-application-settings-dotnet)。  
  
## <a name="properties"></a>屬性  
 `My.Settings` 物件的屬性可存取您應用程式的設定。 若要新增或移除設定，使用**設定設計工具**。  
  
 每個設定都**名稱**，**型別**，**範圍**，和**值**，以及這些設定會決定如何用來存取每個設定屬性會出現在`My.Settings`物件：  
  
-   **名稱**判斷屬性的名稱。  
  
-   **型別**判斷屬性的型別。  
  
-   **範圍**指出屬性是否為唯讀。 如果值為**應用程式**，此屬性是唯讀的; 如果值為**使用者**，屬性是讀寫。  
  
-   **值**是屬性的預設值。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|---|---|  
|`Reload`|重新載入使用者設定從上次儲存的值。|  
|`Save`|儲存目前的使用者設定。|  
  
 `My.Settings`物件也提供進階的屬性和方法，繼承自<xref:System.Configuration.ApplicationSettingsBase>類別。  
  
## <a name="tasks"></a>工作  
 下表列出與工作的範例`My.Settings`物件。  
  
|以|請參閱|  
|---|---|  
|讀取應用程式設定|[如何：在 Visual Basic 中讀取應用程式設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)|  
|變更使用者設定|[如何：在 Visual Basic 中變更使用者設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)|  
|保存使用者設定|[如何：在 Visual Basic 中的使用者設定可持續](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)|  
|建立使用者設定的屬性方格|[如何：建立 Visual Basic 中的使用者設定的屬性方格](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)|  
  
## <a name="example"></a>範例  
 此範例會顯示 `Nickname` 設定的值。  
  
 [!code-vb[VbVbalrMyResources#14](../../../visual-basic/developing-apps/programming/app-settings/codesnippet/VisualBasic/my-settings-object_1.vb)]  
  
 為了確保此範例正常運作，您的應用程式必須具有 `String` 類型的 `Nickname` 設定。  
  
## <a name="see-also"></a>另請參閱
- <xref:System.Configuration.ApplicationSettingsBase>
- [如何：在 Visual Basic 中讀取應用程式設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)
- [如何：在 Visual Basic 中變更使用者設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)
- [如何：在 Visual Basic 中的使用者設定可持續](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)
- [如何：建立 Visual Basic 中的使用者設定的屬性方格](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)
- [管理應用程式設定 (.NET)](/visualstudio/ide/managing-application-settings-dotnet)
