---
UID : NC:ndkpi.NDK_FN_FAST_REGISTER
title : NDK_FN_FAST_REGISTER
author : windows-driver-content
description : The NdkFastRegister (NDK_FN_FAST_REGISTER) function fast-registers an array of adapter logical pages over an existing memory region.
old-location : netvista\ndk_fn_fast_register.htm
old-project : netvista
ms.assetid : 4A37BEF6-8526-430D-AAE6-294363D0EDE7
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
req.alt-api : NdkFastRegister
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


# NDK_FN_FAST_REGISTER callback function
The <i>NdkFastRegister</i> (<i>NDK_FN_FAST_REGISTER</i>) function fast-registers an array of adapter logical pages over an existing memory region.

## Syntax

```
NDK_FN_FAST_REGISTER NdkFnFastRegister;

NTSTATUS NdkFnFastRegister(
  NDK_QP *pNdkQp,
  PVOID RequestContext,
  NDK_MR *pMr,
  ULONG AdapterPageCount,
  CONST NDK_LOGICAL_ADDRESS,
  ULONG FBO,
  SIZE_T Length,
  PVOID BaseVirtualAddress,
  ULONG Flags
)
{...}
```

## Parameters

`*pNdkQp`



`RequestContext`

A  context value to return in the <b>RequestContext</b> member of the <a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a> structure for this request.

`*pMr`



`AdapterPageCount`

The number of pages in the <i>AdapterPageArray</i> parameter. The size of each page in the <i>AdapterPageArray</i> is <b>PAGE_SIZE</b> bytes.

`NDK_LOGICAL_ADDRESS`



`FBO`

The first byte offset (FBO) within the first page. The registered region starts at this offset.

`Length`

The length, in bytes, of the region being registered starting at the FBO. The length must be less than or equal to the total number of bytes that are represented by the first set (<i>AdapterPageCount</i>) of pages that are contained in the <i>AdapterPageArray</i> array minus the FBO.

`BaseVirtualAddress`

The consumer-specified virtual address value to refer to the first byte location of the memory region. This value must be a multiple of <b>PAGE_SIZE</b> plus FBO. So, the allowed values include  FBO, or FBO plus  n times the <b>PAGE_SIZE</b> where n is greater than or equal to zero. Zero is a valid value only if FBO is zero.

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
     <i>NDK_FN_FAST_REGISTER</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The request was posted successfully. A completion entry will be queued to the CQ when the work request is completed.
<dl>
<dt><b>STATUS_CONNECTION_INVALID</b></dt>
</dl>The QP is not connected.
<dl>
<dt><b>STATUS_ACCESS_VIOLATION</b></dt>
</dl>The memory region was not initialized for remote access during fast-register initialization but the fast-register work request specified <b>NDK_OP_FLAG_ALLOW_REMOTE_READ</b> or <b>NDK_OP_FLAG_ALLOW_REMOTE_WRITE</b>.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

<i>NdkFastRegister</i> fast-registers an array of adapter logical pages over an existing memory region that is  initialized for fast registration.

After  this call returns, the memory region token for remote access is available with the <i>NdkGetRemoteTokenFromMr</i> (<a href="..\ndkpi\nc-ndkpi-ndk_fn_get_remote_token_from_mr.md">NDK_FN_GET_REMOTE_TOKEN_FROM_MR</a>)  function of the MR.

<i>NdkFastRegister</i> does not support zero-based virtual addresses.

If the <b>NDK_ADAPTER_FLAG_RDMA_READ_SINK_NOT_REQUIRED</b> flag is not set in the <b>AdapterFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a> structure, an NDK consumer must pass the <b>NDK_OP_FLAG_RDMA_READ_SINK</b> flag when it registers memory that might be used as the sink buffer for an RDMA read request. Certain NDK providers might require the enabling of special access rights on the sink buffer for an RDMA read request. This flag allows such providers to support registration requests appropriately. Note that buffers might be registered for multiple purposes, therefore this flag might be accompanied by others. 

If an NDK consumer passes the <b>NDK_OP_FLAG_RDMA_READ_SINK</b> flag on an adapter for which the <b>NDK_ADAPTER_FLAG_RDMA_READ_SINK_NOT_REQUIRED</b> flag is set in the <b>AdapterFlags</b> member of the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a> structure, the provider is not required to handle the <b>NDK_OP_FLAG_RDMA_READ_SINK</b> flag and must not fail the request  due to the presence of this flag.

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
<a href="..\ndkpi\nc-ndkpi-ndk_fn_get_remote_token_from_mr.md">NDK_FN_GET_REMOTE_TOKEN_FROM_MR</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439851">NDK_ADAPTER_INFO</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_logical_address_mapping.md">NDK_LOGICAL_ADDRESS</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_mr.md">NDK_MR</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_qp.md">NDK_QP</a>
</dt>
<dt>
<a href="..\ndkpi\ns-ndkpi-_ndk_result.md">NDK_RESULT</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/DA2D0FCA-D84B-4599-A560-8F87A0918D99">NDKPI Deferred Processing Scheme</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/2BF6F253-FCB4-4A61-9A67-81092F3C44E4">NDKPI Work Request Posting Requirements</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDK_FN_FAST_REGISTER callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>