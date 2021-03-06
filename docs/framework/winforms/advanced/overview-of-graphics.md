---
title: 圖形概觀
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], using managed interface
- graphics [Windows Forms], about graphics
ms.assetid: a602aef8-a8c8-4c36-9816-74e7bad96a68
ms.openlocfilehash: c569eb249a583ca9f71381210eeb11a8d10b04e5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590197"
---
# <a name="overview-of-graphics"></a>圖形概觀
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 是應用程式開發介面 (API) 構成的 Microsoft Windows 作業系統的子系統。 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 負責顯示螢幕和印表機上的資訊。 正如其名， [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 是 [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] 的後置項，該繪圖裝置介面包含在舊版 Windows 中。  
  
## <a name="managed-class-interface"></a>Managed 類別介面  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] API 透過一組部署為 managed 程式碼的類別。 這組類別稱為*managed 的類別介面*至[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]。 下列命名空間組成 Managed 類別介面：  
  
-   <xref:System.Drawing>  
  
-   <xref:System.Drawing.Drawing2D>  
  
-   <xref:System.Drawing.Imaging>  
  
-   <xref:System.Drawing.Text>  
  
-   <xref:System.Drawing.Printing>  
  
 圖形裝置介面，例如[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]，您可以在螢幕或印表機上顯示資訊，而不須關心特定顯示裝置的詳細資料。 程式設計師會呼叫 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 類別所提供的方法。 這些方法接著會適當地呼叫特定裝置驅動程式。 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 會從圖形硬體隔離應用程式。 這是此隔離會讓程式設計人員能夠建立與裝置無關的應用程式。  
  
## <a name="see-also"></a>另請參閱
- [圖形概觀](../../../../docs/framework/winforms/advanced/graphics-overview-windows-forms.md)
