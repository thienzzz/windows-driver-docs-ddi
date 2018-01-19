---
UID : NC:ndkpi.NDK_FN_WRITE
title : NDK_FN_WRITE
author : windows-driver-content
description : The NdkWrite (NDK_FN_WRITE) function posts a write request on an NDK queue pair (QP).
old-location : netvista\ndk_fn_write.htm
old-project : netvista
ms.assetid : 4AE7E897-556B-40C4-BC12-31D957552690
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
req.alt-api : NdkWrite
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


# NDK_FN_WRITE callback function
The <i>NdkWrite</i> (<i>NDK_FN_WRITE</i>) function posts a write request on an NDK queue pair (QP).

## Syntax

```
NDK_FN_WRITE NdkFnWrite;

NTSTATUS NdkFnWrite(
  NDK_QP *pNdkQp,
  PVOID RequestContext,
  CONST NDK_SGE,
  ULONG nSge,
  UINT64 RemoteAddress,
  UINT32 RemoteToken,
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

`RemoteAddress`

The remote address to write to, provided in the local host's byte order. The NDK consumer might have added an offset to the remotely-provided value.

`RemoteToken`

The remotely-provided memory token, an opaque array of bytes from the NDK consumer.

`Flags`

A bitwise OR of flags which specifies the operations that are allowed. The following flags are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>


## Return Value

The <i>NdkWrite</i> function returns one of the following NTSTATUS codes.
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

<i>NdkWrite</i> posts a write request on a queue pair (QP).

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
<a href="https://msdn.microsoft.com/DA2D0FCA-D84B-4599-A560-8F87A0918D99">NDKPI Deferred Processing Scheme</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/2BF6F253-FCB4-4A61-9A67-81092F3C44E4">NDKPI Work Request Posting Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_WRITE callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>