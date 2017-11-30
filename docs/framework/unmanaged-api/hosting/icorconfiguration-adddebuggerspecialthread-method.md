---
title: "ICorConfiguration::AddDebuggerSpecialThread 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorConfiguration.AddDebuggerSpecialThread
api_location: mscoree.dll
api_type: COM
f1_keywords: AddDebuggerSpecialThread
helpviewer_keywords:
- AddDebuggerSpecialThread method [.NET Framework hosting]
- ICorConfiguration::AddDebuggerSpecialThread method [.NET Framework hosting]
ms.assetid: 1f1e3239-438e-4be9-a3bb-7d0722d3a76d
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2501461267ff7369cd9c48f4cef6cda42063a48b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="icorconfigurationadddebuggerspecialthread-method"></a><span data-ttu-id="aea29-102">ICorConfiguration::AddDebuggerSpecialThread 方法</span><span class="sxs-lookup"><span data-stu-id="aea29-102">ICorConfiguration::AddDebuggerSpecialThread Method</span></span>
<span data-ttu-id="aea29-103">表示特定執行緒應該可以繼續執行，而偵錯工具有 managed 或 unmanaged 偵錯案例期間停止一個應用程式執行偵錯服務。</span><span class="sxs-lookup"><span data-stu-id="aea29-103">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aea29-104">語法</span><span class="sxs-lookup"><span data-stu-id="aea29-104">Syntax</span></span>  
  
```  
HRESULT AddDebuggerSpecialThread (  
    [in] DWORD dwSpecialThreadId  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aea29-105">參數</span><span class="sxs-lookup"><span data-stu-id="aea29-105">Parameters</span></span>  
 `dwSpecialThreadId`  
 <span data-ttu-id="aea29-106">[in]允許繼續執行的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="aea29-106">[in] The ID of the thread that should be allowed to continue executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aea29-107">備註</span><span class="sxs-lookup"><span data-stu-id="aea29-107">Remarks</span></span>  
 <span data-ttu-id="aea29-108">指定的執行緒不會允許執行 managed 程式碼，或以任何方式進入執行階段中。</span><span class="sxs-lookup"><span data-stu-id="aea29-108">The specified thread will not be allowed to run managed code or enter the runtime in any way.</span></span> <span data-ttu-id="aea29-109">舉例來說，這類執行緒會以支援舊版指令碼偵錯工具在處理序執行緒。</span><span class="sxs-lookup"><span data-stu-id="aea29-109">An example of such a thread would be an in-process thread to support legacy script debuggers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aea29-110">需求</span><span class="sxs-lookup"><span data-stu-id="aea29-110">Requirements</span></span>  
 <span data-ttu-id="aea29-111">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="aea29-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aea29-112">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="aea29-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="aea29-113">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="aea29-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="aea29-114">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aea29-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aea29-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aea29-115">See Also</span></span>  
 [<span data-ttu-id="aea29-116">ICorConfiguration 介面</span><span class="sxs-lookup"><span data-stu-id="aea29-116">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)