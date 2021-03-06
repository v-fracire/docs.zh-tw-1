---
title: HOW TO：設定應用程式定義域
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- application domains, configuring
- ApplicationBase property
ms.assetid: 07ea8438-7a34-49f0-a7e8-3d6ff7e4a482
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8989d7695f44b0cd2e8b0ce3ec8bd74a6e802102
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534562"
---
# <a name="how-to-configure-an-application-domain"></a>HOW TO：設定應用程式定義域
您可以使用 <xref:System.AppDomainSetup> 類別向 Common Language Runtime 提供新應用程式定義域的設定資訊。 建立您自己的應用程式定義域時，最重要的屬性是 <xref:System.AppDomainSetup.ApplicationBase%2A>。 其他 **AppDomainSetup** 屬性主要是執行階段主機用來設定特定的應用程式定義域。  
  
 **ApplicationBase** 屬性會定義應用程式的根目錄。 當執行階段需要滿足類型要求時，它會探查組件在 **ApplicationBase** 屬性指定的目錄中是否包含該類型。  
  
> [!NOTE]
>  新的應用程式定義域只繼承建立者的 **ApplicationBase** 屬性。  
  
 以下範例會建立 **AppDomainSetup** 類別的執行個體、使用此類別建立新的應用程式定義域、將資訊寫入主控台，再卸載應用程式定義域。  
  
## <a name="example"></a>範例  
 [!code-cpp[ADApplicationBase#2](../../../samples/snippets/cpp/VS_Snippets_CLR/ADApplicationBase/CPP/source2.cpp#2)]
 [!code-csharp[ADApplicationBase#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADApplicationBase/CS/source2.cs#2)]
 [!code-vb[ADApplicationBase#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADApplicationBase/VB/source2.vb#2)]  
  
## <a name="see-also"></a>另請參閱
- [使用應用程式定義域設計程式](application-domains.md#programming-with-application-domains)
- [使用應用程式定義域](../../../docs/framework/app-domains/use.md)
