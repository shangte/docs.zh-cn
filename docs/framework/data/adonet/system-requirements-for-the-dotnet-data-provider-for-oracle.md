---
title: Oracle 的 .NET Framework 数据提供程序的系统要求
ms.date: 03/30/2017
ms.assetid: 054f76b9-1737-43f0-8160-84a00a387217
ms.openlocfilehash: 664357fb08a6100b8b69d2b4e11edc77cdb81ac7
ms.sourcegitcommit: 8a0fe8a2227af612f8b8941bdb8b19d6268748e7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "71833639"
---
# <a name="system-requirements-for-the-net-framework-data-provider-for-oracle"></a>Oracle 的 .NET Framework 数据提供程序的系统要求

Oracle .NET Framework 数据提供程序需要 Microsoft 数据访问组件 (MDAC) 2.6 版或更高版本。 建议使用 MDAC 2.8 SP1。  
  
 还必须安装 Oracle 8i Release 3 (8.1.7) 客户端或更高版本。  
  
 Oracle 9i 版本之前的 Oracle 客户端软件无法访问 UTF16 数据库，因为 UTF16 是 Oracle 9i 中的一项新功能。 要使用此功能，必须将客户端软件升级到 Oracle 9i 或更高版本。  
  
## <a name="working-with-the-data-provider-for-oracle-and-unicode-data"></a>使用 Oracle 数据提供程序和 Unicode 数据  
 
下面是使用 Oracle 和 Oracle 客户端库的 .NET Framework 数据提供程序时应考虑的与 Unicode 相关的问题列表。 有关更多信息，请参见 Oracle 文档。  
  
### <a name="setting-the-unicode-value-in-a-connection-string-attribute"></a>在连接字符串属性中设置 Unicode 值  

在使用 Oracle 时，可以使用连接字符串属性  
  
`Unicode=True`
  
在 UTF-16 模式下初始化 Oracle 客户端库。 这样可以使 Oracle 客户端库接受 UTF-16（与 UCS-2 非常类似），而不是多字节字符串。 这样，Oracle 数据提供程序始终可以使用任何 Oracle 代码页，不需要进行其他转换工作。 只有使用 Oracle 9i 客户端与包含备选字符集 AL16UTF16 的 Oracle 9i 数据库进行通信时，此配置才有效。 当 Oracle 9i 客户端与 Oracle 9i 服务器通信时，需要额外的资源将 Unicode **CommandText**值转换为 Oracle9i 服务器使用的相应多字节字符集。 如果确定已通过将 `Unicode=True` 添加到连接字符串中而拥有了安全的配置，则可以避免此问题。  
  
### <a name="mixing-versions-of-oracle-client-and-oracle-server"></a>混合版本的 Oracle 客户端和 Oracle 服务器  

当服务器的区域字符集被指定为 AL16UTF16 （Oracle 9i 的默认设置）时，oracle 8i 客户端**无法访问** **NVARCHAR2**或**NCLOB**数据。 因为直到 Oracle 9i 才引入对 UTF-16 字符集的支持，Oracle 8i 客户端无法读取。  
  
### <a name="working-with-utf-8-data"></a>使用 UTF-8 数据  

要设置备选字符集，将注册表项 HKEY_LOCAL_MACHINE\SOFTWARE\ORACLE\HOMEID\NLS_LANG 设置为 UTF8。 有关更多信息，请参见适合您的平台的 Oracle 安装说明。 默认设置为安装 Oracle 客户端软件所使用的语言的主要字符集。 如果设置的语言与所连接的数据库的国家语言字符集不匹配，将使参数和列绑定使用主要数据库字符集发送或接收数据，而不是使用国家字符集。  
  
### <a name="oraclelob-can-only-update-full-characters"></a>OracleLob 只能更新完整字符。  

出于可用性原因， <xref:System.Data.OracleClient.OracleLob>对象继承自 .NET Framework Stream 类，并提供**ReadByte**和**WriteByte**方法。 它还实现了对 Oracle **LOB**对象的各个部分进行处理的方法，如**CopyTo**和**Erase**。 与此相反，Oracle 客户端软件提供了许多 Api 来处理字符**LOB**（**CLOB**和**NCLOB**）。 但是，这些 API 只适用于完整字符。 由于这种差异，Oracle 的数据提供程序实现了对**Read**和**ReadByte**的支持，以便以字节的方式处理 utf-16 数据。 但是， **OracleLob**对象的其他方法只允许全字符操作。  
  
## <a name="see-also"></a>请参阅

- [Oracle 和 ADO.NET](oracle-and-adonet.md)
- [ADO.NET 概述](ado-net-overview.md)
