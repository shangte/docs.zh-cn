---
title: ICorProfilerInfo9 接口
ms.date: 08/06/2019
author: davmason
ms.author: davmason
ms.openlocfilehash: 371e85ce8f5d7b420a30ac842ec658949e47d30e
ms.sourcegitcommit: b11efd71c3d5ce3d9449c8d4345481b9f21392c6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2020
ms.locfileid: "76861640"
---
# <a name="icorprofilerinfo9-interface"></a>ICorProfilerInfo9 接口

[ICorProfilerInfo8](icorprofilerinfo8-interface.md)的子类，提供用于查询有关具有多个本机代码版本的函数的信息的方法。  

## <a name="methods"></a>方法  

| 方法|描述|  
| ------------|-----------------|  
|[GetNativeCodeStartAddresses 方法](icorprofilerinfo9-getnativecodestartaddresses-method.md)| 给定一个 functionId 和 rejitId，枚举此代码当前存在的所有实时编译版本的本机代码起始地址。 |
|[GetILToNativeMapping3 方法](icorprofilerinfo9-getiltonativemapping3-method.md)| 给定本机代码起始地址，返回此实时编译版本的代码的本机到 IL 映射信息。 |
|[GetCodeInfo4 方法](icorprofilerinfo9-getcodeinfo4-method.md)| 给定本机代码起始地址，返回存储此代码的虚拟内存块。 |

## <a name="requirements"></a>需求  
**平台：** 请参阅[支持 .Net Core 的操作系统](../../../core/install/dependencies.md?tabs=netcore30&pivots=os-windows)。  
**头文件：** CorProf.idl、CorProf.h  
**.Net 版本：** [!INCLUDE[net_core](../../../../includes/net-core-22-md.md)]  

## <a name="see-also"></a>另请参阅

- [Profiling 接口](profiling-interfaces.md)
