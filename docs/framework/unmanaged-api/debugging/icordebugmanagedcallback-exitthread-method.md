---
title: ICorDebugManagedCallback::ExitThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitThread
helpviewer_keywords:
- ExitThread method [.NET Framework debugging]
- ICorDebugManagedCallback::ExitThread method [.NET Framework debugging]
ms.assetid: 62db708b-6cf0-45c5-b897-4b5c75bd2505
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8abe1b63aad7b73b3260553550112ded75b77bb9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54537734"
---
# <a name="icordebugmanagedcallbackexitthread-method"></a>ICorDebugManagedCallback::ExitThread 方法
已結束執行緒所執行的 managed 程式碼會告知偵錯工具。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT ExitThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pAppDomain`  
 [in]表示包含 managed 的執行緒的應用程式網域的 ICorDebugAppDomain 物件指標。  
  
 `thread`  
 [in]ICorDebugThread 物件，表示 managed 的執行緒指標。  
  
## <a name="remarks"></a>備註  
 一次`ExitThread`引發回呼時，執行緒不會再出現在 執行緒列舉型別。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorDebug.idl、 CorDebug.h  
  
 **程式庫：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [ICorDebugManagedCallback 介面](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
