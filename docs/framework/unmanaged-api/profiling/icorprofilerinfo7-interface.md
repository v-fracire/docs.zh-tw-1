---
title: ICorProfilerInfo7 介面
ms.date: 03/30/2017
ms.assetid: cf37c462-73c5-412a-a7f8-bb26ca746313
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c33e620b861f1065f95ba9f1f732911723c16f88
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54526271"
---
# <a name="icorprofilerinfo7-interface"></a>ICorProfilerInfo7 介面
[受到 [!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] 和更新版本的支援]  
  
 子類別[ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md)提供方法，以套用新定義模組的中繼資料，並提供存取記憶體中的符號資料流。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[ApplyMetaData 方法](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-applymetadata-method.md)|適用於新所定義的中繼資料`IMetadataEmit::Define*`方法，以指定的模組。|  
|[GetInMemorySymbolsLength 方法](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-getinmemorysymbolslength-method.md)|傳回記憶體中的符號資料流的長度。|  
|[ReadInMemorySymbols](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-readinmemorysymbols.md)|從記憶體中的符號資料流讀取位元組。|  
  
## <a name="requirements"></a>需求  
 **平台：** 請參閱[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorProf.idl, CorProf.h  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a>另請參閱
- [分析介面](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
