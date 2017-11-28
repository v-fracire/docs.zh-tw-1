---
title: "IMetaDataInfo::GetFileMapping 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataInfo.GetFileMapping
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataInfo::GetFileMapping
helpviewer_keywords:
- IMetaDataInfo::GetFileMapping method [.NET Framework metadata]
- GetFileMapping method [.NET Framework metadata]
ms.assetid: 2868dfec-c992-4606-88bb-a8e0b6b18271
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 74f44d366ec4f3848f7c8436e208dcaee3466fe1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatainfogetfilemapping-method"></a><span data-ttu-id="207c2-102">IMetaDataInfo::GetFileMapping 方法</span><span class="sxs-lookup"><span data-stu-id="207c2-102">IMetaDataInfo::GetFileMapping Method</span></span>
<span data-ttu-id="207c2-103">取得記憶體區域的對應的檔，以及對應的類型。</span><span class="sxs-lookup"><span data-stu-id="207c2-103">Gets the memory region of the mapped file, and the type of mapping.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="207c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="207c2-104">Syntax</span></span>  
  
```  
HRESULT GetFileMapping (  
    [out] const void           **ppvData,   
    [out] ULONGLONG            *pcbData,   
    [out] DWORD                *pdwMappingType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="207c2-105">參數</span><span class="sxs-lookup"><span data-stu-id="207c2-105">Parameters</span></span>  
 `ppvData`  
 <span data-ttu-id="207c2-106">[out]對應檔的開頭指標。</span><span class="sxs-lookup"><span data-stu-id="207c2-106">[out] A pointer to the start of the mapped file.</span></span>  
  
 `pcbData`  
 <span data-ttu-id="207c2-107">[out]對應區域的大小。</span><span class="sxs-lookup"><span data-stu-id="207c2-107">[out] The size of the mapped region.</span></span> <span data-ttu-id="207c2-108">如果`pdwMappingType`是`fmFlat`，這是檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="207c2-108">If `pdwMappingType` is `fmFlat`, this is the size of the file.</span></span>  
  
 `pdwMappingType`  
 <span data-ttu-id="207c2-109">[out]A [CorFileMapping](../../../../docs/framework/unmanaged-api/metadata/corfilemapping-enumeration.md)值，指出對應的類型。</span><span class="sxs-lookup"><span data-stu-id="207c2-109">[out] A [CorFileMapping](../../../../docs/framework/unmanaged-api/metadata/corfilemapping-enumeration.md) value that indicates the type of mapping.</span></span> <span data-ttu-id="207c2-110">目前實作的 common language runtime (CLR) 一律會傳回`fmFlat`。</span><span class="sxs-lookup"><span data-stu-id="207c2-110">The current implementation of the common language runtime (CLR) always returns `fmFlat`.</span></span> <span data-ttu-id="207c2-111">其他值被保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="207c2-111">Other values are reserved for future use.</span></span> <span data-ttu-id="207c2-112">不過，您應該一律確認傳回的值，因為可能在未來版本中啟用其他值，或服務版本。</span><span class="sxs-lookup"><span data-stu-id="207c2-112">However, you should always verify the returned value, because other values may be enabled in future versions or service releases.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="207c2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="207c2-113">Return Value</span></span>  
  
|<span data-ttu-id="207c2-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="207c2-114">HRESULT</span></span>|<span data-ttu-id="207c2-115">說明</span><span class="sxs-lookup"><span data-stu-id="207c2-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="207c2-116">所有輸出會填都滿。</span><span class="sxs-lookup"><span data-stu-id="207c2-116">All outputs are filled.</span></span>|  
|`E_INVALIDARG`|<span data-ttu-id="207c2-117">傳遞 NULL 做為引數的值。</span><span class="sxs-lookup"><span data-stu-id="207c2-117">NULL was passed as an argument value.</span></span>|  
|`COR_E_NOTSUPPORTED`|<span data-ttu-id="207c2-118">CLR 實作無法提供記憶體區域的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="207c2-118">The CLR implementation cannot provide information about the memory region.</span></span> <span data-ttu-id="207c2-119">這種情形，原因如下：</span><span class="sxs-lookup"><span data-stu-id="207c2-119">This can happen for the following reasons:</span></span><br /><br /> <span data-ttu-id="207c2-120">-在中繼資料範圍以開啟`ofWrite`或`ofCopyMemory`旗標。</span><span class="sxs-lookup"><span data-stu-id="207c2-120">-   The metadata scope was opened with the `ofWrite` or `ofCopyMemory` flag.</span></span><br /><span data-ttu-id="207c2-121">-在中繼資料範圍已開啟但`ofReadOnly`旗標。</span><span class="sxs-lookup"><span data-stu-id="207c2-121">-   The metadata scope was opened without the `ofReadOnly` flag.</span></span><br /><span data-ttu-id="207c2-122">- [Imetadatadispenser:: Openscopeonmemory](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscopeonmemory-method.md)方法用來開啟僅中繼資料檔案的一部分。</span><span class="sxs-lookup"><span data-stu-id="207c2-122">-   The [IMetaDataDispenser::OpenScopeOnMemory](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscopeonmemory-method.md) method was used to open only the metadata portion of the file.</span></span><br /><span data-ttu-id="207c2-123">-檔案不是可移植執行檔 (PE) 檔案。</span><span class="sxs-lookup"><span data-stu-id="207c2-123">-   The file is not a portable executable (PE) file.</span></span> <span data-ttu-id="207c2-124">**注意：**這些條件取決於 CLR 實作，並可可能會影響在未來的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="207c2-124">**Note:**  These conditions depend on the CLR implementation, and are likely to be weakened in future versions of the CLR.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="207c2-125">備註</span><span class="sxs-lookup"><span data-stu-id="207c2-125">Remarks</span></span>  
 <span data-ttu-id="207c2-126">記憶體的`ppvData`指向無效，只要基礎中繼資料範圍已開啟。</span><span class="sxs-lookup"><span data-stu-id="207c2-126">The memory that `ppvData` points to is valid only as long as the underlying metadata scope is open.</span></span>  
  
 <span data-ttu-id="207c2-127">為了讓您藉由呼叫對應到記憶體中的磁碟上檔案的中繼資料時使用這個方法[imetadatadispenser:: Openscope](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md)方法，您必須指定`ofReadOnly`旗標，而且您必須指定`ofWrite`或`ofCopyMemory`旗標。</span><span class="sxs-lookup"><span data-stu-id="207c2-127">In order for this method to work, when you map the metadata of an on-disk file into memory by calling the [IMetaDataDispenser::OpenScope](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md) method, you must specify the `ofReadOnly` flag and you must not specify the `ofWrite` or `ofCopyMemory` flag.</span></span>  
  
 <span data-ttu-id="207c2-128">選擇每個範圍的檔案對應類型是 CLR 的特定實作的特定項目。</span><span class="sxs-lookup"><span data-stu-id="207c2-128">The choice of file mapping type for each scope is specific to a given implementation of the CLR.</span></span> <span data-ttu-id="207c2-129">無法由使用者設定。</span><span class="sxs-lookup"><span data-stu-id="207c2-129">It cannot be set by the user.</span></span> <span data-ttu-id="207c2-130">目前實作的 clr 一律會傳回`fmFlat`中`pdwMappingType`，但可能會變更在未來版本的 CLR 或未來的指定版本的版本更新服務。</span><span class="sxs-lookup"><span data-stu-id="207c2-130">The current implementation of the CLR always returns `fmFlat` in `pdwMappingType`, but this can change in future versions of the CLR or in future service releases of a given version.</span></span> <span data-ttu-id="207c2-131">請務必檢查傳回的值`pdwMappingType`，因為不同類型會有不同的版面配置和位移。</span><span class="sxs-lookup"><span data-stu-id="207c2-131">You should always check the returned value in `pdwMappingType`, because different types will have different layouts and offsets.</span></span>  
  
 <span data-ttu-id="207c2-132">不支援傳遞任何三個參數為 NULL。</span><span class="sxs-lookup"><span data-stu-id="207c2-132">Passing NULL for any of the three parameters is not supported.</span></span> <span data-ttu-id="207c2-133">方法會傳回`E_INVALIDARG`，和輸出會填滿。</span><span class="sxs-lookup"><span data-stu-id="207c2-133">The method returns `E_INVALIDARG`, and none of the outputs are filled.</span></span> <span data-ttu-id="207c2-134">忽略對應型別或區域的大小，可能會導致程式異常終止。</span><span class="sxs-lookup"><span data-stu-id="207c2-134">Ignoring the mapping type or the size of the region can result in abnormal program termination.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="207c2-135">需求</span><span class="sxs-lookup"><span data-stu-id="207c2-135">Requirements</span></span>  
 <span data-ttu-id="207c2-136">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="207c2-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="207c2-137">**標頭：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="207c2-137">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="207c2-138">**程式庫：**做為 MsCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="207c2-138">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="207c2-139">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="207c2-139">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="207c2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="207c2-140">See Also</span></span>  
 [<span data-ttu-id="207c2-141">IMetaDataInfo 介面</span><span class="sxs-lookup"><span data-stu-id="207c2-141">IMetaDataInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-interface.md)  
 [<span data-ttu-id="207c2-142">CorFileMapping 列舉</span><span class="sxs-lookup"><span data-stu-id="207c2-142">CorFileMapping Enumeration</span></span>](../../../../docs/framework/unmanaged-api/metadata/corfilemapping-enumeration.md)