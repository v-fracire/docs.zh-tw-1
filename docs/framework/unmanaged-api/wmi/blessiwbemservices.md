---
title: "BlessIWbemServices 函式 （Unmanaged API 參考）"
description: "BlessIWbemServices 函式指示使用者認證是否允許存取 IWbemServices 類別。"
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: BlessIWbemServices
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: BlessIWbemServices
helpviewer_keywords: BlessIWbemServices function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 67431d4272ac1da4d400a5552c61cf464680b502
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2017
---
# <a name="blessiwbemservices-function"></a><span data-ttu-id="f295c-103">BlessIWbemServices 函式</span><span class="sxs-lookup"><span data-stu-id="f295c-103">BlessIWbemServices function</span></span>
<span data-ttu-id="f295c-104">表示使用者認證是否允許存取指定[IWbemServices](https://msdn.microsoft.com/library/aa392093(v=vs.85).aspx)類別。</span><span class="sxs-lookup"><span data-stu-id="f295c-104">Indicates whether the user credentials permit access to the specified [IWbemServices](https://msdn.microsoft.com/library/aa392093(v=vs.85).aspx) class.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="f295c-105">語法</span><span class="sxs-lookup"><span data-stu-id="f295c-105">Syntax</span></span>  
  
```  
HRESULT BlessIWbemServices (
   [in] IWbemServices* pIWbemServices,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```  

## <a name="parameters"></a><span data-ttu-id="f295c-106">參數</span><span class="sxs-lookup"><span data-stu-id="f295c-106">Parameters</span></span>

`pIWbemServices`  
<span data-ttu-id="f295c-107">[in]指標[IWbemServices](https://msdn.microsoft.com/library/aa392093(v=vs.85).aspx)權限所需的物件。</span><span class="sxs-lookup"><span data-stu-id="f295c-107">[in] A pointer to the [IWbemServices](https://msdn.microsoft.com/library/aa392093(v=vs.85).aspx) object for which permissions are required.</span></span>

`strUser`  
<span data-ttu-id="f295c-108">[in]使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f295c-108">[in] The user name.</span></span>

`strPassword`  
<span data-ttu-id="f295c-109">[in]與相關聯的密碼`strUser`。</span><span class="sxs-lookup"><span data-stu-id="f295c-109">[in] The password associated with `strUser`.</span></span>

<span data-ttu-id="f295c-110">`strAuthority`[in]使用者的網域名稱。</span><span class="sxs-lookup"><span data-stu-id="f295c-110">`strAuthority` [in] The domain name of the user.</span></span> <span data-ttu-id="f295c-111">請參閱[ConnectServerWmi](connectserverwmi.md)函式，如需詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f295c-111">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

<span data-ttu-id="f295c-112">`impLevel`[in]模擬等級。</span><span class="sxs-lookup"><span data-stu-id="f295c-112">`impLevel` [in] The impersonation level.</span></span>

<span data-ttu-id="f295c-113">`authnLevel`[in]授權層級。</span><span class="sxs-lookup"><span data-stu-id="f295c-113">`authnLevel` [in] The authorization level.</span></span>

## <a name="return-value"></a><span data-ttu-id="f295c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f295c-114">Return value</span></span>

<span data-ttu-id="f295c-115">這個函式傳回下列值會定義在*WinError.h*標頭檔，或者您可以定義它們以常數的形式在程式碼中：</span><span class="sxs-lookup"><span data-stu-id="f295c-115">The following values returned by this function are defined in the *WinError.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="f295c-116">常數</span><span class="sxs-lookup"><span data-stu-id="f295c-116">Constant</span></span>  |<span data-ttu-id="f295c-117">值</span><span class="sxs-lookup"><span data-stu-id="f295c-117">Value</span></span>  |<span data-ttu-id="f295c-118">說明</span><span class="sxs-lookup"><span data-stu-id="f295c-118">Description</span></span>  |
|---------|---------|---------|
| `E_INVALIDARG` | <span data-ttu-id="f295c-119">0x80070057</span><span class="sxs-lookup"><span data-stu-id="f295c-119">0x80070057</span></span> | <span data-ttu-id="f295c-120">一或多個引數均為無效。</span><span class="sxs-lookup"><span data-stu-id="f295c-120">One or more arguments are invalid.</span></span> |
| `E_POINTER` | <span data-ttu-id="f295c-121">0x80004003</span><span class="sxs-lookup"><span data-stu-id="f295c-121">0x80004003</span></span> | <span data-ttu-id="f295c-122">`pIWbemServices` 為 `null`。</span><span class="sxs-lookup"><span data-stu-id="f295c-122">`pIWbemServices` is `null`.</span></span> | 
| `E_FAIL` | <span data-ttu-id="f295c-123">0x80000008</span><span class="sxs-lookup"><span data-stu-id="f295c-123">0x80000008</span></span> | <span data-ttu-id="f295c-124">發生意外的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f295c-124">An unspecified error has occurred.</span></span> |
| `E_OUTOFMEMORY` | <span data-ttu-id="f295c-125">0x80000002</span><span class="sxs-lookup"><span data-stu-id="f295c-125">0x80000002</span></span> | <span data-ttu-id="f295c-126">記憶體不足，無法使用執行作業。</span><span class="sxs-lookup"><span data-stu-id="f295c-126">Insufficient memory is available to perform the operation.</span></span> | 
| `S_OK` | <span data-ttu-id="f295c-127">0</span><span class="sxs-lookup"><span data-stu-id="f295c-127">0</span></span> | <span data-ttu-id="f295c-128">函式呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="f295c-128">The function call was successful.</span></span> | 

## <a name="requirements"></a><span data-ttu-id="f295c-129">需求</span><span class="sxs-lookup"><span data-stu-id="f295c-129">Requirements</span></span>  
 <span data-ttu-id="f295c-130">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f295c-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f295c-131">**標頭：** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="f295c-131">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="f295c-132">**.NET framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f295c-132">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f295c-133">請參閱</span><span class="sxs-lookup"><span data-stu-id="f295c-133">See also</span></span>  
[<span data-ttu-id="f295c-134">WMI 和效能計數器 （Unmanaged API 參考）</span><span class="sxs-lookup"><span data-stu-id="f295c-134">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)