---
title: AssemblyAttributesGoHere
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: AssemblyAttributesGoHere
api_location: alink.dll
api_type: COM
f1_keywords: AssemblyAttributesGoHere
helpviewer_keywords:
- AssemblyAttributesGoHere type
- Alink API, AssemblyAttributesGoHere type
ms.assetid: 7b26fcb6-94f4-4f09-933e-b33efe451f4f
topic_type: apiref
caps.latest.revision: "4"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9577ecb1f987d86527a96723f45f09509c55d5cb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="assemblyattributesgohere"></a><span data-ttu-id="d7d92-102">AssemblyAttributesGoHere</span><span class="sxs-lookup"><span data-stu-id="d7d92-102">AssemblyAttributesGoHere</span></span>
<span data-ttu-id="d7d92-103">供 ALink 用來做為儲存自訂屬性相關資訊的預留位置。</span><span class="sxs-lookup"><span data-stu-id="d7d92-103">Used by ALink as a placeholder to store information about custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7d92-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7d92-104">Syntax</span></span>  
  
```  
AssemblyAttributesGoHere  
```  
  
## <a name="remarks"></a><span data-ttu-id="d7d92-105">備註</span><span class="sxs-lookup"><span data-stu-id="d7d92-105">Remarks</span></span>  
 <span data-ttu-id="d7d92-106">這個類型的參考可能會內嵌在來源中包含組件自訂屬性的 netmodule 中。</span><span class="sxs-lookup"><span data-stu-id="d7d92-106">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="d7d92-107">從一個或多個包含這些類型參考的 netmodule 建置組件資訊清單時，ALink 會使用附加至這些參考的資訊來發出真正的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="d7d92-107">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="d7d92-108">因此，這個類型永遠不會具現化，而其參考只會用來做為建置流程的一部分，在最後的組件中並沒有任何用途。</span><span class="sxs-lookup"><span data-stu-id="d7d92-108">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>  
  
 <span data-ttu-id="d7d92-109">這個類型的參考會指出與安全性無關且不是多用途的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="d7d92-109">References to this type indicate custom attributes that are not security related and are not multiple-use.</span></span>  
  
 <span data-ttu-id="d7d92-110">這些類型會在 .NET Framework 中標示為「內部」，其位於 <xref:System.Runtime.CompilerServices>。</span><span class="sxs-lookup"><span data-stu-id="d7d92-110">These types are marked "internal" within the .NET Framework, and are located in <xref:System.Runtime.CompilerServices>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7d92-111">需求</span><span class="sxs-lookup"><span data-stu-id="d7d92-111">Requirements</span></span>  
 <span data-ttu-id="d7d92-112">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="d7d92-112">mscorlib.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7d92-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7d92-113">See Also</span></span>  
 [<span data-ttu-id="d7d92-114">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="d7d92-114">AssemblyAttributesGoHereM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoherem.md)  
 [<span data-ttu-id="d7d92-115">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="d7d92-115">AssemblyAttributesGoHereS</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheres.md)  
 [<span data-ttu-id="d7d92-116">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="d7d92-116">AssemblyAttributesGoHereSM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheresm.md)