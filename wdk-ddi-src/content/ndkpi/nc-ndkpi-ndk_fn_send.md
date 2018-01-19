---
UID : NC:ndkpi.NDK_FN_SEND
title : NDK_FN_SEND
author : windows-driver-content
description : The NdkSend (NDK_FN_SEND) function posts a send request on an NDK queue pair (QP).
old-location : netvista\ndk_fn_send.htm
old-project : netvista
ms.assetid : 6EDF95F1-AE00-4931-9B18-E316D56D57AF
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
req.alt-api : NdkSend
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


# NDK_FN_SEND callback function
The <i>NdkSend</i> (<i>NDK_FN_SEND</i>) function posts a send request on an NDK queue pair (QP).

## Syntax

```
NDK_FN_SEND NdkFnSend;

NTSTATUS NdkFnSend(
  NDK_QP *pNdkQp,
  PVOID RequestContext,
  CONST NDK_SGE,
  ULONG nSge,
  ULONG Flags
)
{...}
```

## Parameters

`*pNdkQp`



`RequestContext`

A context value to be returned in the <b>RequestContext</b> member of the <a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a> structure for this request.

`NDK_SGE`



`nSge`

The number of SGE structures in the array  that is specified in the <i>pSgl</i>
parameter.

`Flags`

A bitwise OR of flags which specifies the operations that are allowed. The following flags are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>


## Return Value

The 
     <i>NdkSend</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The send request was posted successfully. A completion entry will be queued to the completion queue (CQ) when the work request is completed.

<dl>
<dt><b>STATUS_CONNECTION_INVALID</b></dt>
</dl>The queue pair (QP) is not connected.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

<i>NdkSend</i> posts a send request on a queue pair (QP).

You can use the <b>NDK_OP_FLAG_SEND_AND_SOLICIT_EVENT</b> flag if you issue multiple, related send requests. Set this flag on the last request in the group of related send requests.

An NDK consumer can use this flag when issuing multiple, related send requests. The NDK consumer sets this flag only on the last, related send request. The peer will receive all the send requests as normal. However, when the peer receives the last send request (the request with the <b>NDK_OP_FLAG_SEND_AND_SOLICIT_EVENT</b> flag set), the completion queue for the peer generates a notification. The notification is generated after the receive request completes. This flag has no meaning to the receiver (peer) unless the receiver has previously called the <i>NdkArmCq</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_arm_cq.md">NDK_FN_ARM_CQ</a>) function with the notification type set to <b>NDK_CQ_NOTIFY_SOLICITED</b>.

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
<a href="..\ndkpi\ns-ndkpi-_ndk_qp.md">NDK_QP</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_sge.md">NDK_SGE</a>
</dt>
<dt>
<a href="..\ndkpi\nc-ndkpi-ndk_fn_arm_cq.md">NDK_FN_ARM_CQ</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/DA2D0FCA-D84B-4599-A560-8F87A0918D99">NDKPI Deferred Processing Scheme</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/2BF6F253-FCB4-4A61-9A67-81092F3C44E4">NDKPI Work Request Posting Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_SEND callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>