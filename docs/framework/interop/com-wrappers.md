---
title: COM 包装
ms.date: 03/30/2017
helpviewer_keywords:
- wrapper classes
- COM interop, COM wrappers
- COM wrappers
- COM, wrappers
- interoperation with unmanaged code, COM wrappers
- COM callable wrappers
ms.assetid: e56c485b-6b67-4345-8e66-fd21835a6092
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 57483f099bb71a1ab685cedf148d4343c12983dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33390518"
---
# <a name="com-wrappers"></a>COM 包装
COM 在以下几个重要方面与 .NET Framework 对象模型存在差别：  
  
-   COM 对象的客户端必需管理这些对象的生存期；公共语言运行时管理其环境中对象的生存期。  
  
-   COM 对象的客户端通过对提供服务的接口发出请求并取回接口指针来发现服务是否可用。 .NET 对象的客户端可以使用反射来获取对象功能的说明。  
  
-   NET 对象驻留在由 .NET Framework 执行环境管理的内存中。 出于性能原因，执行环境可以在内存中来回移动对象，并更新所移动对象的所有引用。 非管理的客户端在获取指向对象的指针后，依赖于该对象以保留在相同位置。 这些客户端没有机制来处理位置不固定的对象。  
  
 为了克服这些差异，运行时提供了包装类，使托管和非管理的客户端认为它们在各自的环境中调用对象。 每当托管客户端对某个 COM 对象调用方法时，运行时就会创建一个[运行时可调用包装器](runtime-callable-wrapper.md) (RCW)。 除此之外，RCW 还会提取托管和非托管引用机制之间的差异。 该运行时还创建了一个 [COM 可调用包装器](com-callable-wrapper.md) (CCW) 来逆转此过程，使 COM 客户端能够对 .NET 对象无缝地调用方法。 如下图所示，调用代码的性质确定运行时创建的包装类。  
  
 ![COM 包装器概述](media/bidirectional.gif "双向")  
COM 包装器概述  
  
 大多数情况下，运行时生成的标准 RCW 或 CCW 都可为跨 COM 和.NET Framework 之间边界的调用提供充分的封送处理。 使用自定义属性，可以选择性地调整运行时表示托管和非托管代码的方式。  
  
## <a name="see-also"></a>请参阅  
 [高级 COM 互操作性](https://msdn.microsoft.com/library/3ada36e5-2390-4d70-b490-6ad8de92f2fb(v=vs.100))  
 [运行时可调用包装器](runtime-callable-wrapper.md)  
 [COM 可调用包装器](com-callable-wrapper.md)  
 [自定义标准包装器](https://msdn.microsoft.com/library/c40d089b-6a3c-41b5-a20d-d760c215e49d(v=vs.100))  
 [如何：自定义运行时可调用包装器](https://msdn.microsoft.com/library/4a4bb3da-4d60-4517-99f2-78d46a681732(v=vs.100))
