---
title: "StrongNameSignatureVerificationEx2 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRStrongName2.StrongNameSignatureVerificationEx2
api_location: mscoree.dll
api_type: COM
f1_keywords: StrongNameSignatureVerificationEx2
helpviewer_keywords:
- StrongNameSignatureVerificationEx2 method, ICLRStrongName2 interface [.NET Framework hosting]
- ICLRStrongName2::StrongNameSignatureVerificationEx2 method [.NET Framework hosting]
ms.assetid: dfd4133f-a074-4db3-a7ee-4f250fe9ad3a
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 823eac67a53c4534a12122b118ac46bb91530d1b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="strongnamesignatureverificationex2-method"></a><span data-ttu-id="ca972-102">StrongNameSignatureVerificationEx2 方法</span><span class="sxs-lookup"><span data-stu-id="ca972-102">StrongNameSignatureVerificationEx2 Method</span></span>
<span data-ttu-id="ca972-103">驗證簽章是強式名稱組件，並提供從 ECMA 金鑰對應至實際的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ca972-103">Verifies the signature of a strongly named assembly, and provides a mapping from the ECMA key to a real key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca972-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca972-104">Syntax</span></span>  
  
```  
HRESULT StrongNameSignatureVerificationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  BOOLEAN   fForceVerification,    [in]  BYTE      *pbEcmaPublicKey,  
    [in]  DWORD     cbEcmaPublicKey,  
    [out] BOOLEAN   *pfWasVerified  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ca972-105">參數</span><span class="sxs-lookup"><span data-stu-id="ca972-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="ca972-106">[in]可攜式執行檔 （.exe 或.dll） 檔案要驗證的組件路徑。</span><span class="sxs-lookup"><span data-stu-id="ca972-106">[in] The path to the portable executable (.exe or .dll) file for the assembly to be verified.</span></span>  
  
 `fForceVerification`  
 <span data-ttu-id="ca972-107">[in]`true`執行驗證，即使它是必要的登錄設定會覆寫，否則`false`。</span><span class="sxs-lookup"><span data-stu-id="ca972-107">[in] `true` to perform verification, even if it is necessary to override registry settings; otherwise, `false`.</span></span>  
  
 `pbEcmaPublicKey`  
 <span data-ttu-id="ca972-108">[in]實際的索引鍵的 ECMA 公開金鑰對應的指標會用於驗證。</span><span class="sxs-lookup"><span data-stu-id="ca972-108">[in] A pointer to the mapping from the ECMA public key to the real key used for verification.</span></span>  
  
 `cbEcmaPublicKey`  
 <span data-ttu-id="ca972-109">[in]真實的 ECMA 公用金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="ca972-109">[in] The length of the real ECMA public key.</span></span>  
  
 `pfWasVerified`  
 <span data-ttu-id="ca972-110">[out]`true`強式名稱簽章已通過驗證，否則如果`false`。</span><span class="sxs-lookup"><span data-stu-id="ca972-110">[out] `true` if the strong name signature was verified; otherwise, `false`.</span></span> <span data-ttu-id="ca972-111">這個參數也會設為`false`如果驗證已成功登錄設定所造成。</span><span class="sxs-lookup"><span data-stu-id="ca972-111">This parameter is also set to `false` if the verification was successful due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ca972-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca972-112">Return Value</span></span>  
 <span data-ttu-id="ca972-113">`S_OK`如果驗證成功。否則，表示失敗的 HRESULT 值 (請參閱[常見的 HRESULT 值](http://go.microsoft.com/fwlink/?LinkId=213878)清單)。</span><span class="sxs-lookup"><span data-stu-id="ca972-113">`S_OK` if the verification was successful; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca972-114">需求</span><span class="sxs-lookup"><span data-stu-id="ca972-114">Requirements</span></span>  
 <span data-ttu-id="ca972-115">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ca972-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca972-116">**標頭：** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="ca972-116">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="ca972-117">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="ca972-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ca972-118">**.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca972-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca972-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca972-119">See Also</span></span>  
 [<span data-ttu-id="ca972-120">StrongNameSignatureVerification 方法</span><span class="sxs-lookup"><span data-stu-id="ca972-120">StrongNameSignatureVerification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md)  
 [<span data-ttu-id="ca972-121">StrongNameSignatureVerificationEx 方法</span><span class="sxs-lookup"><span data-stu-id="ca972-121">StrongNameSignatureVerificationEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md)  
 [<span data-ttu-id="ca972-122">ICLRStrongName 介面</span><span class="sxs-lookup"><span data-stu-id="ca972-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)