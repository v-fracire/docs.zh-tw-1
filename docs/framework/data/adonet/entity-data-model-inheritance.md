---
title: 實體資料模型：繼承
ms.date: 03/30/2017
ms.assetid: 42c7ef24-710a-4af9-8493-cd41c399ecb0
ms.openlocfilehash: 1a5ac0e4f5d4b8fe58b5d8577a27b26163d94952
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54684199"
---
# <a name="entity-data-model-inheritance"></a>實體資料模型：繼承
Entity Data Model (EDM) 支援的繼承[實體類型](../../../../docs/framework/data/adonet/entity-type.md)。 EDM 中的繼承類似於物件導向程式設計語言中的類別繼承。 像物件導向語言中的類別，，您也可以在概念模型中定義實體類型 (*衍生型別*)，繼承自另一個實體類型 (*基底型別*)。 不過，不同於物件導向程式設計中的類別，概念模型中的衍生的類型一律會繼承所有[屬性](../../../../docs/framework/data/adonet/property.md)並[導覽屬性](../../../../docs/framework/data/adonet/navigation-property.md)基底類型。 您不能覆寫衍生型別中的繼承屬性。  
  
 在概念模型中，您可以組建繼承階層，其中的衍生型別繼承自另一種衍生型別。 頂端的階層 (root type) 不是衍生的型別階層架構中) 的類型稱為*根型別*。 繼承階層架構內[實體索引鍵](../../../../docs/framework/data/adonet/entity-key.md)必須定義根型別上。  
  
 您不可建置衍生型別繼承自多個型別的繼承階層。 例如，在具有 `Book` 實體類型的概念模型中，您可以定義分別繼承自 `FictionBook` 的衍生型別 `NonFictionBook` 和 `Book`。 不過，您可能無法定義同時繼承自 `FictionBook` 和 `NonFictionBook` 型別的型別。  
  
## <a name="example"></a>範例  
 下圖顯示包含四種實體類型 (`Book`、`FictionBook`、`Publisher` 和 `Author`) 的概念模型： `FictionBook` 實體類型為衍生型別，繼承自 `Book` 實體類型。 `FictionBook` 型別繼承自 `ISBN (Key)`、`Title` 和 `Revision` 屬性，並且定義稱為 `Genre` 的額外屬性。  
  
 ![Inheritance](../../../../docs/framework/data/adonet/media/inheritanceexample.gif "InheritanceExample")  
  
 [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)會使用稱為概念結構定義語言的特定領域語言 (DSL) ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 來定義概念模型。 下列 CSDL 定義實體類型 `FictionBook`，此實體類型繼承自 `Book` 型別 (如上圖所示)：  
  
 [!code-xml[EDM_Example_Model#DerivedType](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books5.edmx#derivedtype)]  
  
## <a name="see-also"></a>另請參閱
- [實體資料模型索引鍵概念](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [實體資料模型](../../../../docs/framework/data/adonet/entity-data-model.md)
