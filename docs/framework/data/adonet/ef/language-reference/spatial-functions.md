---
title: 空間函式
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: 09402633c5e7f591a534992fc92655e6a2d1d88d
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904480"
---
# <a name="spatial-functions"></a>空間函式
空間型別沒有任何常值格式。 不過，您可以使用標準 Entity Framework 函式 (使用 Well-Known Text 格式的字串所呼叫)。 例如，下列函式呼叫可建立幾何點：  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 <xref:System.Data.Common.CommandTrees.ExpressionBuilder.Spatial.SpatialEdmFunctions>方法具有所有空間標準 Entity Framework 方法。 按一下相關方法，以查看應將哪些參數傳遞至函式。
