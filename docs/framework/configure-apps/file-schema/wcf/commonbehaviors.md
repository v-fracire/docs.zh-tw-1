---
title: <commonBehaviors>
ms.date: 03/30/2017
ms.assetid: 5260aeca-388d-4e82-94c0-124fa8054cf5
ms.openlocfilehash: 73bf759fd3dfa87398aa74de93160a4ffce08eba
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2019
ms.locfileid: "55268752"
---
# <a name="commonbehaviors"></a>\<commonBehaviors>
`commonBehaviors` 區段只能定義在 machine.config 檔中。 它會定義兩個名為 `endpointBehaviors` 和 `serviceBehaviors` 的子集合。  每個集合會定義分別由所有 WCF 端點和電腦上的服務的行為項目。 在 `endpointBehaviors` 中定義的行為只會套用至用戶端，在 `serviceBehaviors` 中定義的行為只會套用至服務。 如果 `commonBehaviors` 和 `behaviors` 區段中都有定義某個行為，則會優先使用 `behaviors` 區段中的行為。
