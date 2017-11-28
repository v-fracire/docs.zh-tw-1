---
title: "已被取代的 CLR 裝載介面和 Coclass"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- interfaces [.NET Framework hosting], version 1
- .NET Framework 1.1, hosting interfaces
- hosting interfaces [.NET Framework], version 1
- .NET Framework 1.0, hosting interfaces
ms.assetid: 7b3d2755-cbab-4160-bc69-eb85791e38c7
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 4714183eb79a25639dae6824a1d27eb1ca6bb009
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="deprecated-clr-hosting-interfaces-and-coclasses"></a><span data-ttu-id="223c3-102">已被取代的 CLR 裝載介面和 Coclass</span><span class="sxs-lookup"><span data-stu-id="223c3-102">Deprecated CLR Hosting Interfaces and Coclasses</span></span>
<span data-ttu-id="223c3-103">本節描述 unmanaged 介面主機可以使用整合 common language runtime (CLR) 在.NET framework 1.0 和 1.1 版中將其應用程式。</span><span class="sxs-lookup"><span data-stu-id="223c3-103">This section describes the interfaces that unmanaged hosts can use to integrate the common language runtime (CLR) in the .NET Framework versions 1.0 and 1.1 into their applications.</span></span> <span data-ttu-id="223c3-104">這些介面提供主應用程式設定和執行階段載入處理序的方法。</span><span class="sxs-lookup"><span data-stu-id="223c3-104">These interfaces provide methods for a host to configure and load the runtime into a process.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="223c3-105">本章節內容</span><span class="sxs-lookup"><span data-stu-id="223c3-105">In This Section</span></span>  
 <span data-ttu-id="223c3-106">IAppDomainSetup</span><span class="sxs-lookup"><span data-stu-id="223c3-106">IAppDomainSetup</span></span>  
 <span data-ttu-id="223c3-107">提供方法來設定主機<xref:System.AppDomain>。</span><span class="sxs-lookup"><span data-stu-id="223c3-107">Provides methods for the host to configure an <xref:System.AppDomain>.</span></span>  
  
 [<span data-ttu-id="223c3-108">ICeeFileGen 類別</span><span class="sxs-lookup"><span data-stu-id="223c3-108">ICeeFileGen Class</span></span>](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md)  
 <span data-ttu-id="223c3-109">（已被取代）提供建立原生可攜式執行檔 (PE) 的功能。</span><span class="sxs-lookup"><span data-stu-id="223c3-109">(Deprecated) Provides functionality for creating a native portable executable (PE) file.</span></span>  
  
 [<span data-ttu-id="223c3-110">ICorRuntimeHost 介面</span><span class="sxs-lookup"><span data-stu-id="223c3-110">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)  
 <span data-ttu-id="223c3-111">提供方法來進行 CLR 設定主機。</span><span class="sxs-lookup"><span data-stu-id="223c3-111">Provides methods for the host to configure CLR settings.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="223c3-112">相關章節</span><span class="sxs-lookup"><span data-stu-id="223c3-112">Related Sections</span></span>  
 [<span data-ttu-id="223c3-113">CLR 裝載介面</span><span class="sxs-lookup"><span data-stu-id="223c3-113">CLR Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)  
 <span data-ttu-id="223c3-114">包含的主題將描述裝載介面提供與.NET Framework 2.0 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="223c3-114">Contains topics that describe the hosting interfaces provided with the .NET Framework version 2.0 and later versions.</span></span>