---
UID : NC:ndkpi.NDK_FN_CREATE_QP
title : NDK_FN_CREATE_QP
author : windows-driver-content
description : The NdkCreateQp (NDK_FN_CREATE_QP) function creates an NDK queue pair (QP) object.
old-location : netvista\ndk_fn_create_qp.htm
old-project : netvista
ms.assetid : 8B601E53-9BE9-4D84-819E-3B0BD07560BC
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_WWAN_VISIBLE_PROVIDERS, NDIS_WWAN_VISIBLE_PROVIDERS, *PNDIS_WWAN_VISIBLE_PROVIDERS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : ndkpi.h
req.include-header : Ndkpi.h
req.target-type : Windows
req.target-min-winverclnt : None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdkCreateQp
req.alt-loc : ndkpi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : NDIS_WWAN_VISIBLE_PROVIDERS, *PNDIS_WWAN_VISIBLE_PROVIDERS
---


# NDK_FN_CREATE_QP callback function
The <i>NdkCreateQp</i> (<i>NDK_FN_CREATE_QP</i>) function creates an NDK queue pair (QP) object.

## Syntax

```
NDK_FN_CREATE_QP NdkFnCreateQp;

NTSTATUS NdkFnCreateQp(
  NDK_PD *pNdkPd,
  NDK_CQ *pReceiveCq,
  NDK_CQ *pInitiatorCq,
  PVOID QPContext,
  ULONG ReceiveQueueDepth,
  ULONG InitiatorQueueDepth,
  ULONG MaxReceiveRequestSge,
  ULONG MaxInitiatorRequestSge,
  ULONG InlineDataSize,
  NDK_FN_CREATE_COMPLETION CreateCompletion,
  PVOID RequestContext,
  NDK_QP **ppNdkQp
)
{...}
```

## Parameters

`*pNdkPd`



`*pReceiveCq`



`*pInitiatorCq`



`QPContext`

A context value to be returned in the <b>QPContext</b> member of the  <a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a> structure for all requests that are posted over this QP.

`ReceiveQueueDepth`

The maximum number of receive requests that can be outstanding over the QP. This value must be less than or equal to the value in the  <b>MaxReceiveQueueDepth</b> member of the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a> structure.

`InitiatorQueueDepth`

The maximum number of initiator requests that can be outstanding over the QP. This value must be less than or equal to the value in the  <b>MaxInitiatorQueueDepth</b> member of the  NDK_ADAPTER_INFO structure.

`MaxReceiveRequestSge`

The maximum number of SGEs that can be supported in a single receive request. This value must be less than or equal to the value in the  <b>MaxReceiveRequestSge</b> member of the  NDK_ADAPTER_INFO structure.

`MaxInitiatorRequestSge`

The maximum number of SGEs that can be supported in a single initiator request. This value must be less than or equal to the value in the  <b>MaxInitiatorRequestSge</b> member of the  NDK_ADAPTER_INFO structure.

`InlineDataSize`

The maximum amount of inline data in bytes that can be sent in a single send or write request. This value must be less than or equal to the value in the  <b>MaxInlineDataSize</b> member of the  NDK_ADAPTER_INFO structure.

`CreateCompletion`

A pointer to an <i>NdkCreateCompletion</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>) function that completes the creation of an NDK object.

`RequestContext`

A context value that the NDK provider passes back to the <i>NdkCreateCompletion</i> function that is specified in the <i>CreateCompletion</i> parameter.

`**ppNdkQp`




## Return Value

The 
     <i>NdkCreateQp</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The QP object was created successfully and returned with the <i>*ppNdkQp</i> parameter.
<dl>
<dt><b>STATUS_PENDING</b></dt>
</dl> The operation is pending and will be completed later. The provider will call the function specified in the <i>CreateCompletion</i> parameter(<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>) to complete the pending operation.
 
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>The request failed because the requested <i>ReceiveQueueDepth</i>, <i>InitiatorQueueDepth</i>,  <i>MaxReceiveRequestSge</i>, <i>MaxInitiatorRequestSge</i>, or <i>InlineDataSize</i> are not within the limits that are specified in the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a> structure.
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>The request failed due to insufficient resources. 
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

The <i>NdkCreateQp</i> function creates an   NDK queue pair (QP) object.  A QP consists of a receive queue and an initiator queue. The receive queue is used to  post receive requests. An initiator queue is used for initiating send, bind, fast-register, read, write, and invalidate requests.

If the function returns STATUS_SUCCESS, the created object is returned in the <i>ppNdkQp</i> parameter. If <i>NdkCreateQp</i> returns STATUS_PENDING, the created object is returned by the <i>NdkCreateCompletion</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>) function that is specified in the <i>CreateCompletion</i> parameter.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndkpi.h (include Ndkpi.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_cq.md">NDK_CQ</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_pd.md">NDK_PD</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_qp.md">NDK_QP</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a>
</dt>
<dt>
<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/94993523-D0D7-441E-B95C-417800840BAC">NDKPI Object Lifetime Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_CREATE_QP callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>