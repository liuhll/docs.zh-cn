---
title: "GetDemultiplexedStub 函数 （非托管 API 参考）"
description: "GetDemultiplexedStub 函数将创建的对象转发器接收器，以帮助客户端在从 Windows 管理接收异步调用。"
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: GetDemultiplexedStub
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: GetDemultiplexedStub
helpviewer_keywords: GetDemultiplexedStub function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a81101acbf65546ea068e6b5a0e8d9045aaadc71
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2017
---
# <a name="getdemultiplexedstub-function"></a><span data-ttu-id="30d9a-103">GetDemultiplexedStub 函数</span><span class="sxs-lookup"><span data-stu-id="30d9a-103">GetDemultiplexedStub function</span></span>
<span data-ttu-id="30d9a-104">创建的对象转发器接收器，以帮助客户端在从 Windows 管理接收异步调用。</span><span class="sxs-lookup"><span data-stu-id="30d9a-104">Creates an object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="30d9a-105">语法</span><span class="sxs-lookup"><span data-stu-id="30d9a-105">Syntax</span></span>  
  
```  
HRESULT GetDemultiplexedStub (
   [in] IUnknown*    pObject, 
   [in] boolean      isLocal, 
   [out] IUnknown**  ppObject
); 
```  

## <a name="parameters"></a><span data-ttu-id="30d9a-106">参数</span><span class="sxs-lookup"><span data-stu-id="30d9a-106">Parameters</span></span>

`pObject`  
<span data-ttu-id="30d9a-107">[in]指向客户端的过程中实现的[IWbemObjectSink](https://msdn.microsoft.com/en-us/library/aa391787(v=vs.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="30d9a-107">[in] A pointer to the client's in-process implementation of [IWbemObjectSink](https://msdn.microsoft.com/en-us/library/aa391787(v=vs.85).aspx).</span></span>

`isLocal`  
<span data-ttu-id="30d9a-108">[in]一个标志，指示该事件是否本地 (`true`); 否则为`false`。</span><span class="sxs-lookup"><span data-stu-id="30d9a-108">[in] A flag that indicates whether the event is local (`true`); otherwise, `false`.</span></span>

`ppObject`  
<span data-ttu-id="30d9a-109">[out]对象的转发器接收器有助于客户端在从 Windows 管理接收异步调用。</span><span class="sxs-lookup"><span data-stu-id="30d9a-109">[out] A object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>

## <a name="return-value"></a><span data-ttu-id="30d9a-110">返回值</span><span class="sxs-lookup"><span data-stu-id="30d9a-110">Return value</span></span>

<span data-ttu-id="30d9a-111">如果函数成功，则返回值是`S_OK`(0)。</span><span class="sxs-lookup"><span data-stu-id="30d9a-111">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="30d9a-112">如果函数失败，返回值将为非零错误代码。</span><span class="sxs-lookup"><span data-stu-id="30d9a-112">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="30d9a-113">若要获得扩展的错误信息，调用[GetErrorInfo](geterrorinfo.md)函数。</span><span class="sxs-lookup"><span data-stu-id="30d9a-113">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
    
## <a name="requirements"></a><span data-ttu-id="30d9a-114">要求</span><span class="sxs-lookup"><span data-stu-id="30d9a-114">Requirements</span></span>  
 <span data-ttu-id="30d9a-115">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="30d9a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30d9a-116">**标头：** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="30d9a-116">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="30d9a-117">**.NET framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="30d9a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30d9a-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="30d9a-118">See also</span></span>  
[<span data-ttu-id="30d9a-119">WMI 和性能计数器 （非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="30d9a-119">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)