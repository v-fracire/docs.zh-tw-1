---
title: ODBC 資料類型對應
ms.date: 03/30/2017
ms.assetid: 43c35d32-831d-480f-a150-78f7e869d17f
ms.openlocfilehash: f57ba69a03837805f168cf33a9b8060633a6330f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724222"
---
# <a name="odbc-data-type-mappings"></a>ODBC 資料類型對應
下表顯示來自 .NET Framework Data Provider for ODBC ([!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]) 之資料型別的推斷 <xref:System.Data.Odbc> 型別。 同時也一併列出 <xref:System.Data.Odbc.OdbcDataReader> 具型別的存取子方法。  
  
|ODBC 型別|[!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 類型|[!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 具型別的存取子|  
|---------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|  
|SQL_BIGINT|Int64|GetInt64()|  
|SQL_BINARY|Byte[]|GetBytes()|  
|SQL_BIT|Boolean|GetBoolean()|  
|SQL_CHAR|String<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_DECIMAL|Decimal|GetDecimal()|  
|SQL_DOUBLE|Double|GetDouble()|  
|SQL_GUID|Guid|GetGuid()|  
|SQL_INTEGER|Int32|GetInt32()|  
|SQL_LONG_VARCHAR|String<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_LONGVARBINARY|Byte[]|GetBytes()|  
|SQL_NUMERIC|Decimal|GetDecimal()|  
|SQL_REAL|Single|GetFloat()|  
|SQL_SMALLINT|Int16|GetInt16()|  
|SQL_TINYINT|Byte|GetByte()|  
|SQL_TYPE_TIMES|DateTime|GetDateTime()|  
|SQL_TYPE_TIMESTAMP|DateTime|GetDateTime()|  
|SQL_VARBINARY|Byte[]|GetBytes()|  
|SQL_WCHAR|String<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_WLONGVARCHAR|String<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_WVARCHAR|String<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
  
## <a name="see-also"></a>另請參閱
- [在 ADO.NET 中擷取和修改資料](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [ADO.NET Managed 提供者和 DataSet 開發人員中心](https://go.microsoft.com/fwlink/?LinkId=217917)
