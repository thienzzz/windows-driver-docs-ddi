---
UID : NC:ndkpi.NDK_FN_CREATE_SHARED_ENDPOINT
title : NDK_FN_CREATE_SHARED_ENDPOINT
author : windows-driver-content
description : The NdkCreateSharedEndpoint (NDK_FN_CREATE_SHARED_ENDPOINT) function creates an NDK shared endpoint.
old-location : netvista\ndk_fn_create_shared_endpoint.htm
old-project : netvista
ms.assetid : FE65B384-387E-4E04-8CF4-9C218F83A0C8
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
req.alt-api : NdkCreateSharedEndpoint
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


# NDK_FN_CREATE_SHARED_ENDPOINT callback function
The <i>NdkCreateSharedEndpoint</i> (<i>NDK_FN_CREATE_SHARED_ENDPOINT</i>) function creates an NDK shared endpoint.

## Syntax

```
NDK_FN_CREATE_SHARED_ENDPOINT NdkFnCreateSharedEndpoint;

NTSTATUS NdkFnCreateSharedEndpoint(
  NDK_ADAPTER *pNdkAdapter,
  CONST PSOCKADDR,
  ULONG AddressLength,
  NDK_FN_CREATE_COMPLETION CreateCompletion,
  PVOID RequestContext,
  NDK_SHARED_ENDPOINT **ppNdkSharedEndpoint
)
{...}
```

## Parameters

`*pNdkAdapter`



`PSOCKADDR`



`AddressLength`

The size, in bytes, of local address data at the <i>pAddress</i> parameter.

`CreateCompletion`

A pointer to an <i>NdkCreateCompletion</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>) function that completes the creation of an NDK object.

`RequestContext`

A context value that the NDK provider passes back to the <i>NdkCreateCompletion</i> function that is specified in the <i>CreateCompletion</i> parameter.

`**ppNdkSharedEndpoint`




## Return Value

The 
     <i>NdkCreateSharedEndpoint</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The shared endpoint object was  created successfully and returned with the <i>*ppNdkSharedEndpoint</i> parameter.
<dl>
<dt><b>STATUS_PENDING</b></dt>
</dl> The operation is pending and will be completed later. The provider will call the function specified in the <i>CreateCompletion</i> parameter (<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>) to complete the pending operation.
 
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>The request failed due to insufficient resources. 
<dl>
<dt><b>STATUS_SHARING_VIOLATION</b></dt>
</dl>	  The request failed because the specified local address is already in use.
<dl>
<dt><b>STATUS_TOO_MANY_ADDRESSES</b></dt>
</dl>The request failed because the consumer specified a local port number of zero, and the Network Direct provider was unable to allocate a port from the ephemeral port space (ports 49152-65535.)
<dl>
<dt><b>STATUS_INVALID_ADDRESS</b></dt>
</dl>	The request failed because the specified local address is not a valid address for the adapter. 
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

The <i>NdkCreateSharedEndpoint</i> function creates an NDK shared endpoint to use as the local address for multiple outgoing connections that are destined to different remote addresses. This is analogous to having multiple incoming connections to the same local address that are represented by a listener object.

 If the function returns STATUS_SUCCESS, the created object is returned in the <i>ppNdkSharedEndpoint</i> parameter. If <i>NdkCreateSharedEndpoint</i> returns STATUS_PENDING, the created object is returned by the <i>NdkCreateCompletion</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>) function that is specified in the <i>CreateCompletion</i> parameter.

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
<a href="..\ndkpi\ns-ndkpi-_ndk_adapter.md">NDK_ADAPTER</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_adapter_dispatch.md">NDK_ADAPTER_DISPATCH</a>
</dt>
<dt>
<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_completion.md">NDK_FN_CREATE_COMPLETION</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_shared_endpoint.md">NDK_SHARED_ENDPOINT</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/94993523-D0D7-441E-B95C-417800840BAC">NDKPI Object Lifetime Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_CREATE_SHARED_ENDPOINT callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>