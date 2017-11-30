---
title: "IMetaDataTables::GetTableInfo 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataTables.GetTableInfo
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataTables::GetTableInfo
helpviewer_keywords:
- IMetaDataTables::GetTableInfo method [.NET Framework metadata]
- GetTableInfo method [.NET Framework metadata]
ms.assetid: 50cbe557-2322-41aa-8e0d-f967602eaa0f
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 0f4ccd9bbd1c7caa9bbeb548176d834dc8844213
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatatablesgettableinfo-method"></a><span data-ttu-id="f6c75-102">IMetaDataTables::GetTableInfo 方法</span><span class="sxs-lookup"><span data-stu-id="f6c75-102">IMetaDataTables::GetTableInfo Method</span></span>
<span data-ttu-id="f6c75-103">取得名稱、 資料列大小、 資料列數目、 資料行數與指定之資料表的索引鍵資料行索引。</span><span class="sxs-lookup"><span data-stu-id="f6c75-103">Gets the name, row size, number of rows, number of columns, and key column index of the specified table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6c75-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6c75-104">Syntax</span></span>  
  
```  
HRESULT GetTableInfo (  
    [in]  ULONG       ixTbl,  
    [out] ULONG       *pcbRow,  
    [out] ULONG       *pcRows,  
    [out] ULONG       *pcCols,  
    [out] ULONG       *piKey,  
    [out] const char  **ppName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f6c75-105">參數</span><span class="sxs-lookup"><span data-stu-id="f6c75-105">Parameters</span></span>  
 `ixTbl`  
 <span data-ttu-id="f6c75-106">[in]資料表的識別項来傳回其屬性。</span><span class="sxs-lookup"><span data-stu-id="f6c75-106">[in] The identifier of the table whose properties to return.</span></span>  
  
 `pcbRow`  
 <span data-ttu-id="f6c75-107">[out]大小，以位元組為單位的資料表資料列的指標。</span><span class="sxs-lookup"><span data-stu-id="f6c75-107">[out] A pointer to the size, in bytes, of a table row.</span></span>  
  
 `pcRows`  
 <span data-ttu-id="f6c75-108">[out]資料表中的資料列號碼的指標。</span><span class="sxs-lookup"><span data-stu-id="f6c75-108">[out] A pointer to the number of rows in the table.</span></span>  
  
 `pcCols`  
 <span data-ttu-id="f6c75-109">[out]資料表中的資料行編號的指標。</span><span class="sxs-lookup"><span data-stu-id="f6c75-109">[out] A pointer to the number of columns in the table.</span></span>  
  
 `piKey`  
 <span data-ttu-id="f6c75-110">[out]指向的索引鍵資料行或-1，如果資料表沒有索引鍵資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="f6c75-110">[out] A pointer to the index of the key column, or -1 if the table has no key column.</span></span>  
  
 `ppName`  
 <span data-ttu-id="f6c75-111">[out]指向資料表名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="f6c75-111">[out] A pointer to a pointer to the table name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6c75-112">需求</span><span class="sxs-lookup"><span data-stu-id="f6c75-112">Requirements</span></span>  
 <span data-ttu-id="f6c75-113">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6c75-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6c75-114">**標頭：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f6c75-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f6c75-115">**程式庫：**做為 MsCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="f6c75-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f6c75-116">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6c75-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6c75-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6c75-117">See Also</span></span>  
 [<span data-ttu-id="f6c75-118">IMetaDataTables 介面</span><span class="sxs-lookup"><span data-stu-id="f6c75-118">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="f6c75-119">IMetaDataTables2 介面</span><span class="sxs-lookup"><span data-stu-id="f6c75-119">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)