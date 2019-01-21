---
title: CLRDATA_IL_ADDRESS_MAP 結構
ms.date: 01/16/2019
api.name:
- CLRDATA_IL_ADDRESS_MAP Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure
helpviewer.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 94ebef007cf2893b63383aa4657d382728d3c759
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416324"
---
# <a name="clrdatailaddressmap-structure"></a><span data-ttu-id="9f4eb-102">CLRDATA_IL_ADDRESS_MAP 結構</span><span class="sxs-lookup"><span data-stu-id="9f4eb-102">CLRDATA_IL_ADDRESS_MAP Structure</span></span>

<span data-ttu-id="9f4eb-103">IL 定義位址對應。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-103">Defines an IL to address mapping.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="9f4eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f4eb-104">Syntax</span></span>

```
typedef struct
{
    ULONG32 ilOffset;
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
    CLRDataSourceType type;
} CLRDATA_IL_ADDRESS_MAP;
```

## <a name="members"></a><span data-ttu-id="9f4eb-105">成員</span><span class="sxs-lookup"><span data-stu-id="9f4eb-105">Members</span></span>

| <span data-ttu-id="9f4eb-106">成員</span><span class="sxs-lookup"><span data-stu-id="9f4eb-106">Member</span></span>         | <span data-ttu-id="9f4eb-107">描述</span><span class="sxs-lookup"><span data-stu-id="9f4eb-107">Description</span></span>                                            |
| -------------- | ------------------------------------------------------ |
| `ilOffset`     | <span data-ttu-id="9f4eb-108">包含的位址範圍的 IL 位移</span><span class="sxs-lookup"><span data-stu-id="9f4eb-108">IL offset for the contained address range</span></span>              |
| `startAddress` | <span data-ttu-id="9f4eb-109">範圍的起始位址。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-109">The start address of the range.</span></span>                        |
| `endAddress`   | <span data-ttu-id="9f4eb-110">範圍結束位址。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-110">The end address of the range.</span></span>                          |
| `type`         | <span data-ttu-id="9f4eb-111">資料的類型。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-111">The type of the data.</span></span> <span data-ttu-id="9f4eb-112">目前不使用此值</span><span class="sxs-lookup"><span data-stu-id="9f4eb-112">This value is currently not used</span></span> |

## <a name="remarks"></a><span data-ttu-id="9f4eb-113">備註</span><span class="sxs-lookup"><span data-stu-id="9f4eb-113">Remarks</span></span>

<span data-ttu-id="9f4eb-114">此結構內執行階段，而且不會公開透過任何標頭或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-114">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="9f4eb-115">若要使用它，將結構定義成指定上述其中`CLRDATA_ADDRESS`是 64 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-115">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f4eb-116">需求</span><span class="sxs-lookup"><span data-stu-id="9f4eb-116">Requirements</span></span>

<span data-ttu-id="9f4eb-117">**平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9f4eb-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="9f4eb-118">**標頭：** 無</span><span class="sxs-lookup"><span data-stu-id="9f4eb-118">**Header:** None</span></span>  
<span data-ttu-id="9f4eb-119">**程式庫：** 無</span><span class="sxs-lookup"><span data-stu-id="9f4eb-119">**Library:** None</span></span>   
<span data-ttu-id="9f4eb-120">**.NET framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="9f4eb-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f4eb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f4eb-121">See Also</span></span>

- [<span data-ttu-id="9f4eb-122">CLRDataSourceType 列舉</span><span class="sxs-lookup"><span data-stu-id="9f4eb-122">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="9f4eb-123">偵錯</span><span class="sxs-lookup"><span data-stu-id="9f4eb-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="9f4eb-124">偵錯結構</span><span class="sxs-lookup"><span data-stu-id="9f4eb-124">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)