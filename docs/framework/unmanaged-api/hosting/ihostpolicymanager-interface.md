---
title: "IHostPolicyManager 介面"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostPolicyManager
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostPolicyManager
helpviewer_keywords: IHostPolicyManager interface [.NET Framework hosting]
ms.assetid: 8c4aa124-5e00-46d9-b1e8-57ba6574bb0d
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8f49474f1a75af91ac5296be866914e05732e755
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="ihostpolicymanager-interface"></a><span data-ttu-id="b7e44-102">IHostPolicyManager 介面</span><span class="sxs-lookup"><span data-stu-id="b7e44-102">IHostPolicyManager Interface</span></span>
<span data-ttu-id="b7e44-103">提供方法，通知主應用程式中的案例中的 common language runtime (CLR) 執行的動作會中止，逾時或失敗。</span><span class="sxs-lookup"><span data-stu-id="b7e44-103">Provides methods that notify the host of the actions the common language runtime (CLR) performs in case of aborts, timeouts, or failures.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b7e44-104">方法</span><span class="sxs-lookup"><span data-stu-id="b7e44-104">Methods</span></span>  
  
|<span data-ttu-id="b7e44-105">方法</span><span class="sxs-lookup"><span data-stu-id="b7e44-105">Method</span></span>|<span data-ttu-id="b7e44-106">說明</span><span class="sxs-lookup"><span data-stu-id="b7e44-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b7e44-107">OnDefaultAction 方法</span><span class="sxs-lookup"><span data-stu-id="b7e44-107">OnDefaultAction Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-ondefaultaction-method.md)|<span data-ttu-id="b7e44-108">通知主機在 CLR 即將採取的呼叫所指定的預設動作[iclrpolicymanager:: Setdefaultaction](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md)回應執行緒中止或<xref:System.AppDomain>卸載。</span><span class="sxs-lookup"><span data-stu-id="b7e44-108">Notifies the host that the CLR is about to take the default action specified by a call to [ICLRPolicyManager::SetDefaultAction](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md) in response to a thread abort or <xref:System.AppDomain> unload.</span></span>|  
|[<span data-ttu-id="b7e44-109">OnFailure 方法</span><span class="sxs-lookup"><span data-stu-id="b7e44-109">OnFailure Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-onfailure-method.md)|<span data-ttu-id="b7e44-110">通知主機在 CLR 即將採取的動作呼叫所指定[iclrpolicymanager:: Setactiononfailure](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md)資源配置或回收失敗的回應。</span><span class="sxs-lookup"><span data-stu-id="b7e44-110">Notifies the host that the CLR is about to take the action specified by a call to [ICLRPolicyManager::SetActionOnFailure](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md) in response to a resource allocation or reclamation failure.</span></span>|  
|[<span data-ttu-id="b7e44-111">OnTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="b7e44-111">OnTimeout Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-ontimeout-method.md)|<span data-ttu-id="b7e44-112">通知主機在 CLR 即將採取的動作呼叫所指定[iclrpolicymanager:: Setactionontimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md)回應逾時。</span><span class="sxs-lookup"><span data-stu-id="b7e44-112">Notifies the host that the CLR is about to take the action specified by a call to [ICLRPolicyManager::SetActionOnTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md) in response to a timeout.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b7e44-113">需求</span><span class="sxs-lookup"><span data-stu-id="b7e44-113">Requirements</span></span>  
 <span data-ttu-id="b7e44-114">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b7e44-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7e44-115">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b7e44-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b7e44-116">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="b7e44-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b7e44-117">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7e44-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7e44-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7e44-118">See Also</span></span>  
 [<span data-ttu-id="b7e44-119">EClrFailure 列舉</span><span class="sxs-lookup"><span data-stu-id="b7e44-119">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)  
 [<span data-ttu-id="b7e44-120">EClrOperation 列舉</span><span class="sxs-lookup"><span data-stu-id="b7e44-120">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)  
 [<span data-ttu-id="b7e44-121">EPolicyAction 列舉</span><span class="sxs-lookup"><span data-stu-id="b7e44-121">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)  
 [<span data-ttu-id="b7e44-122">ICLRPolicyManager 介面</span><span class="sxs-lookup"><span data-stu-id="b7e44-122">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [<span data-ttu-id="b7e44-123">裝載介面</span><span class="sxs-lookup"><span data-stu-id="b7e44-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)