---
UID : NC:ndkpi.NDK_FN_SEND_AND_INVALIDATE
title : NDK_FN_SEND_AND_INVALIDATE
author : windows-driver-content
description : The NdkSendAndInvalidate (NDK_FN_SEND_AND_INVALIDATE) function posts a send request on an NDK queue pair (QP) and supplies a token to be invalidated at the remote peer upon receive completion.
old-location : netvista\ndk_fn_send_and_invalidate.htm
old-project : netvista
ms.assetid : 7E344DFA-159A-4084-905A-0A0F9F102051
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_WWAN_VISIBLE_PROVIDERS, NDIS_WWAN_VISIBLE_PROVIDERS, *PNDIS_WWAN_VISIBLE_PROVIDERS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : ndkpi.h
req.include-header : Ndkpi.h
req.target-type : Windows
req.target-min-winverclnt : None supported,Supported in NDIS 6.40 and later.
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDK_FN_SEND_AND_INVALIDATE
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


# NDK_FN_SEND_AND_INVALIDATE callback function
The <i>NdkSendAndInvalidate</i> (<i>NDK_FN_SEND_AND_INVALIDATE</i>) function posts a send request on an NDK queue pair (QP) and supplies a token to be invalidated at the remote peer upon receive completion.

## Syntax

```
NDK_FN_SEND_AND_INVALIDATE NdkFnSendAndInvalidate;

NTSTATUS NdkFnSendAndInvalidate(
  NDK_QP *pNdkQp,
  PVOID RequestContext,
  CONST NDK_SGE,
  ULONG nSge,
  ULONG Flags,
  UINT32 RemoteToken
)
{...}
```

## Parameters

`*pNdkQp`



`RequestContext`

A context value to be returned in the <b>RequestContext</b> member of the <a href="..\ndkpi\ns-ndkpi-_ndk_result_ex.md">NDK_RESULT_EX</a> structure for this request.

`NDK_SGE`



`nSge`

The number of SGE structures in the array  that is specified in the <i>pSgl</i>
parameter.

`Flags`

A bitwise OR of flags that specify the operations that are allowed. The following flags are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>

`RemoteToken`

The remote token to be invalidated at the peer upon receive completion. The NDK provider at the receiving peer must abort the connection, as specified by lower layer transport rules, if an invalid token was specified by the sending peer.


## Return Value

The 
     <i>NdkSendAndInvalidate</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The request was posted successfully. A completion entry will be queued to the completion queue (CQ) when the work request is completed.

<dl>
<dt><b>STATUS_CONNECTION_INVALID</b></dt>
</dl>The queue pair (QP) is not connected.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

You can use the <b>NDK_OP_FLAG_SEND_AND_SOLICIT_EVENT</b> flag if you issue multiple, related send requests. Set this flag on the last request in the group.

An NDK consumer can use this flag when issuing multiple, related send requests. The NDK consumer sets this flag only on the last, related send request. The peer will receive all the send requests as normal. However, when the peer receives the last send request (the request with the <b>NDK_OP_FLAG_SEND_AND_SOLICIT_EVENT</b> flag set), the completion queue for the peer generates a notification. The notification is generated after the receive request completes. This flag has no meaning to the receiver (peer) unless the receiver has previously called the <i>NdkArmCq</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_arm_cq.md">NDK_FN_ARM_CQ</a>) function with the notification type set to <b>NDK_CQ_NOTIFY_SOLICITED</b>. 

The NDK consumer should ensure that the <i>NdkSendAndInvalidate</i> function is not called if the receiving peer does not support remote invalidation. The consumer must either negotiate this capability using an out-of-band mechanism or not use this function. If the consumer violates this requirement, the provider's behavior is undefined.

Any <a href="..\ndkpi\ns-ndkpi-_ndk_result_ex.md">NDK_RESULT_EX</a> structure that is added to a completion queue as a result of a call to this function must specify <b>NdkOperationTypeSend</b> for the <b>Type</b> member. Note that you do not need to specify a value for the <b>TypeSpecificCompletionOutput</b> member of the <b>NDK_RESULT_EX</b> structure.

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
<a href="..\ndkpi\nc-ndkpi-ndk_fn_arm_cq.md">NDK_FN_ARM_CQ</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_result_ex.md">NDK_RESULT_EX</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_qp.md">NDK_QP</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_sge.md">NDK_SGE</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/87150E2F-64F2-4EAB-A8B3-8E77622BE36C">NDKPI Completion Handling Requirements</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/DA2D0FCA-D84B-4599-A560-8F87A0918D99">NDKPI Deferred Processing Scheme</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/2BF6F253-FCB4-4A61-9A67-81092F3C44E4">NDKPI Work Request Posting Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_SEND_AND_INVALIDATE callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>