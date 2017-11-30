---
title: "COR_PRF_RUNTIME_TYPE 列舉"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_RUNTIME_TYPE Enumeration
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_RUNTIME_TYPE
helpviewer_keywords: COR_PRF_RUNTIME_TYPE enumeration [.NET Framework profiling]
ms.assetid: 35449514-333f-4918-9c60-7aa198d655d2
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 1a16cfe2f0f2c05721be4d4630729cfbbff98c8f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="corprfruntimetype-enumeration"></a><span data-ttu-id="67673-102">COR_PRF_RUNTIME_TYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="67673-102">COR_PRF_RUNTIME_TYPE Enumeration</span></span>
<span data-ttu-id="67673-103">包含值，表示 common language runtime (CLR) 版本： 桌面或 CoreCLR，Silverlight 中使用。</span><span class="sxs-lookup"><span data-stu-id="67673-103">Contains values that indicate the version of the common language runtime (CLR): desktop or CoreCLR, which is used in Silverlight.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67673-104">語法</span><span class="sxs-lookup"><span data-stu-id="67673-104">Syntax</span></span>  
  
```  
typedef enum  
{  
    COR_PRF_DESKTOP_CLR = 0x1,  
    COR_PRF_CORE_CLR    = 0x2,  
} COR_PRF_RUNTIME_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="67673-105">成員</span><span class="sxs-lookup"><span data-stu-id="67673-105">Members</span></span>  
  
|<span data-ttu-id="67673-106">成員</span><span class="sxs-lookup"><span data-stu-id="67673-106">Member</span></span>|<span data-ttu-id="67673-107">說明</span><span class="sxs-lookup"><span data-stu-id="67673-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_DESKTOP_CLR`|<span data-ttu-id="67673-108">桌面的 clr 版本。</span><span class="sxs-lookup"><span data-stu-id="67673-108">The desktop version of the CLR.</span></span>|  
|`COR_PRF_CORE_CLR`|<span data-ttu-id="67673-109">核心使用 Silverlight 中的 clr 版本。</span><span class="sxs-lookup"><span data-stu-id="67673-109">The core version of the CLR, used in Silverlight.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="67673-110">備註</span><span class="sxs-lookup"><span data-stu-id="67673-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67673-111">需求</span><span class="sxs-lookup"><span data-stu-id="67673-111">Requirements</span></span>  
 <span data-ttu-id="67673-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="67673-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67673-113">**標頭：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="67673-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="67673-114">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="67673-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="67673-115">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67673-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67673-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67673-116">See Also</span></span>  
 [<span data-ttu-id="67673-117">分析列舉</span><span class="sxs-lookup"><span data-stu-id="67673-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)