---
title: ICorDebug::DebugActiveProcess 方法
ms.date: 03/30/2017
api_name:
- ICorDebug.DebugActiveProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::DebugActiveProcess
helpviewer_keywords:
- DebugActiveProcess method [.NET Framework debugging]
- ICorDebug::DebugActiveProcess method [.NET Framework debugging]
ms.assetid: fdab0ade-7f56-4fa2-b3ef-f7a1d2852bba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9cdee0d111c18d7bdf8c91ed4cbb368504ca3b2d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538306"
---
# <a name="icordebugdebugactiveprocess-method"></a>ICorDebug::DebugActiveProcess 方法
將偵錯工具附加至現有的處理序。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT DebugActiveProcess (  
    [in]  DWORD               id,  
    [in]  BOOL                win32Attach,  
    [out] ICorDebugProcess    **ppProcess  
);  
```  
  
#### <a name="parameters"></a>參數  
 `id`  
 [in]偵錯工具後要附加到處理序的識別碼。  
  
 `win32Attach`  
 [in]布林值，設為`true`如果偵錯工具應該做為處理序的 Win32 偵錯工具，並分派 unmanaged 的回呼中; 否則`false`。  
  
 `ppProcess`  
 [out]表示要附加偵錯工具的程序的"ICorDebugProcess 」 物件的位址指標。  
  
## <a name="remarks"></a>備註  
 不支援 Win9x 和非 x86 平台上，例如 IA-64 架構和 amd64 平台的 interop 偵錯。  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorDebug.idl、 CorDebug.h  
  
 **程式庫：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [ICorDebug 介面](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
