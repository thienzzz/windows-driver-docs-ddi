---
UID : NC:ndkpi.NDK_FN_CONNECT_WITH_SHARED_ENDPOINT
title : NDK_FN_CONNECT_WITH_SHARED_ENDPOINT
author : windows-driver-content
description : The NdkConnectWithSharedEndpoint (NDK_FN_CONNECT_WITH_SHARED_ENDPOINT) function initiates an NDK connect request from a shared local address to a remote address.
old-location : netvista\ndk_fn_connect_with_shared_endpoint.htm
old-project : netvista
ms.assetid : E97C0B87-C031-4C91-8FFF-86B5E8324FB8
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
req.alt-api : NdkConnectWithSharedEndpoint
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


# NDK_FN_CONNECT_WITH_SHARED_ENDPOINT callback function
The <i>NdkConnectWithSharedEndpoint</i> (<i>NDK_FN_CONNECT_WITH_SHARED_ENDPOINT</i>) function initiates an NDK connect request from a shared local address to a remote address.

## Syntax

```
NDK_FN_CONNECT_WITH_SHARED_ENDPOINT NdkFnConnectWithSharedEndpoint;

NTSTATUS NdkFnConnectWithSharedEndpoint(
  NDK_CONNECTOR *pNdkConnector,
  NDK_QP *pNdkQp,
  NDK_SHARED_ENDPOINT *pNdkSharedEndpoint,
  CONST PSOCKADDR,
  ULONG DestAddressLength,
  ULONG InboundReadLimit,
  ULONG OutboundReadLimit,
  CONST PVOID,
  ULONG PrivateDataLength,
  NDK_FN_REQUEST_COMPLETION RequestCompletion,
  PVOID RequestContext
)
{...}
```

## Parameters

`*pNdkConnector`



`*pNdkQp`



`*pNdkSharedEndpoint`



`PSOCKADDR`



`DestAddressLength`

The size, in bytes,  of destination address data at the <i>pDestAddress.</i> parameter.

`InboundReadLimit`

The consumer-supplied maximum number of incoming in-progress read operations to allow on the QP. If the underlying provider has a lower <b>MaxInboundReadLimit</b> value in the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a> structure, then the provider will cap the consumer-supplied value to the provider maximum. If the peer has a lower <i>OutboundReadLimit</i> value, then the provider will use that value as the effective <i>InboundReadLimit</i>. The consumer can retrieve the effective <i>InboundReadLimit</i> by calling the <i>NdkGetConnectionData</i> function (<a href="..\ndkpi\nc-ndkpi-ndk_fn_get_connection_data.md">NDK_FN_GET_CONNECTION_DATA</a>).

`OutboundReadLimit`

The consumer-supplied maximum number of outgoing in-progress read operations to allow on the QP. If the underlying provider has a lower <b>MaxOutboundReadLimit</b> value  in the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a> structure, then the provider will cap the consumer supplied value to the provider maximum. If the peer has a lower <i>InboundReadLimit</i>, then the provider will use that value as the effective <i>OutboundReadLimit</i>. The     consumer can retrieve the effective <i>OutboundReadLimit</i> by calling the <i>NdkGetConnectionData</i> function (<a href="..\ndkpi\nc-ndkpi-ndk_fn_get_connection_data.md">NDK_FN_GET_CONNECTION_DATA</a>).

`PVOID`



`PrivateDataLength`

The length, in bytes, of the private data that is provided in the <i>pPrivateData</i> parameter.

`RequestCompletion`

A pointer to a request completion callback routine <i>NdkRequestCompletion</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_request_completion.md">NDK_FN_REQUEST_COMPLETION</a>).

`RequestContext`

A context value to pass to the <i>Context</i> parameter of the  callback function that is specified in the <i>RequestCompletion</i> parameter.


## Return Value

The 
     <i>NdkConnectWithSharedEndpoint</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The connect request was completed successfully.
<dl>
<dt><b>STATUS_PENDING</b></dt>
</dl> The operation is pending and will be completed later. The driver will call the specified <i>RequestCompletion</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_request_completion.md">NDK_FN_REQUEST_COMPLETION</a>) function to complete the pending operation.
 
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>The  request failed due to insufficient resources. 
<dl>
<dt><b>STATUS_NETWORK_UNREACHABLE</b></dt>
</dl>The request failed because the remote network was not reachable. The connection attempt may be retried. 
<dl>
<dt><b>STATUS_HOST_UNREACHABLE</b></dt>
</dl>The request failed because the remote system was not reachable. The connection attempt may be retried. 
<dl>
<dt><b>STATUS_CONNECTION_REFUSED</b></dt>
</dl>The request failed because the remote system refused the connection request. This can be due to lack of listener, backlog limits, or the peer actively rejecting the connection request. The connection attempt may be retried. 
<dl>
<dt><b>STATUS_IO_TIMEOUT</b></dt>
</dl>The request failed because the connection request timed out. The connection attempt may be retried. Timeout values are selected by Network Direct providers to match their respective network characteristics.
<dl>
<dt><b>STATUS_ADDRESS_ALREADY_EXISTS</b></dt>
</dl>The request failed because a connection with the combination of local address, local port, remote address, and remote port already exists. 
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

<i>NdkConnectWithSharedEndpoint</i> initiates a connect request from a shared local address to a specific remote address. <i>NdkConnectWithSharedEndpoint</i> allows an NDK consumer to use the same local address (for example, 10.1.1.1:9999) for many outgoing connections when the destination addresses for the connections are different.

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
<a href="..\ndkpi\ns-ndkpi-_ndk_connector.md">NDK_CONNECTOR</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_connector_dispatch.md">NDK_CONNECTOR_DISPATCH</a>
</dt>
<dt>
<a href="..\ndkpi\nc-ndkpi-ndk_fn_get_connection_data.md">NDK_FN_GET_CONNECTION_DATA</a>
</dt>
<dt>
<a href="..\ndkpi\nc-ndkpi-ndk_fn_request_completion.md">NDK_FN_REQUEST_COMPLETION</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_qp.md">NDK_QP</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_shared_endpoint.md">NDK_SHARED_ENDPOINT</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/94993523-D0D7-441E-B95C-417800840BAC">NDKPI Object Lifetime Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_CONNECT_WITH_SHARED_ENDPOINT callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>