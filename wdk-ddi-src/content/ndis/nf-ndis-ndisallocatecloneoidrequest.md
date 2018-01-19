---
UID : NF:ndis.NdisAllocateCloneOidRequest
title : NdisAllocateCloneOidRequest function
author : windows-driver-content
description : The NdisAllocateCloneOidRequest function allocates memory for a new NDIS_OID_REQUEST structure and copies all the information from an existing NDIS_OID_REQUEST structure to the newly allocated structure.
old-location : netvista\ndisallocatecloneoidrequest.htm
old-project : netvista
ms.assetid : 426ff4f4-7924-4115-9f66-b4152e2ba5bb
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisAllocateCloneOidRequest
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Desktop
req.target-min-winverclnt : Supported in NDIS 6.0 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisAllocateCloneOidRequest
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : Irql_OID_Function
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ndis.lib
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisAllocateCloneOidRequest function
The 
  <b>NdisAllocateCloneOidRequest</b> function allocates memory for a new 
  <a href="..\ndis\ns-ndis-_ndis_oid_request.md">NDIS_OID_REQUEST</a> structure and copies all the
  information from an existing NDIS_OID_REQUEST structure to the newly allocated structure.

## Syntax

````
NDIS_STATUS NdisAllocateCloneOidRequest(
  _In_  NDIS_HANDLE       SourceHandle,
  _In_  PNDIS_OID_REQUEST Request,
  _In_  UINT              PoolTag,
  _Out_ PNDIS_OID_REQUEST *CloneRequest
);
````

## Parameters

`SourceHandle`

An NDIS handle that identifies a filter module or an intermediate driver's protocol
     binding.

`OidRequest`



`PoolTag`

A kernel pool tag. The tag is a string, delimited by single quotation marks, with as many as four
     characters, usually specified in reverse order.

`ClonedOidRequest`




## Return Value

<b>NdisAllocateClonedRequest</b> can return one of the following status values:
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>NDIS successfully allocated an NDIS_OID_REQUEST structure. The 
       <i>CloneRequest</i> parameter contains a pointer to the NDIS_OID_REQUEST structure.
<dl>
<dt><b>NDIS_STATUS_INVALID_PARAMETER</b></dt>
</dl>The allocation request failed because the NDIS handle specified at 
       <i>SourceHandle</i> is not valid.
<dl>
<dt><b>NDIS_STATUS_RESOURCES</b></dt>
</dl>The allocation request failed because NDIS did not have sufficient resources to complete the
       allocation request.
<dl>
<dt><b>NDIS_STATUS_FAILURE</b></dt>
</dl>The driver failed to allocate the cloned structure for reasons other than those in the preceding
       list.

## Remarks

To forward a request down to the underlying drivers, an NDIS intermediate driver or filter driver must
    call 
    <b>NdisAllocateCloneOidRequest</b> to allocate a cloned 
    <a href="..\ndis\ns-ndis-_ndis_oid_request.md">NDIS_OID_REQUEST</a> structure. A filter driver
    or intermediate driver should not forward the original NDIS_OID_REQUEST structure to underlying
    drivers.

<b>NdisAllocateCloneOidRequest</b> allocates new memory and copies the data from an existing
    NDIS_OID_REQUEST structure to the new structure.

The driver must subsequently call the 
    <a href="..\ndis\nf-ndis-ndisfreecloneoidrequest.md">NdisFreeCloneOidRequest</a> function
    to free the NDIS_OID_REQUEST structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** | Irql_OID_Function |

## See Also

<dl>
<dt>
<a href="..\ndis\ns-ndis-_ndis_oid_request.md">NDIS_OID_REQUEST</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisfreecloneoidrequest.md">NdisFreeCloneOidRequest</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisAllocateCloneOidRequest function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>