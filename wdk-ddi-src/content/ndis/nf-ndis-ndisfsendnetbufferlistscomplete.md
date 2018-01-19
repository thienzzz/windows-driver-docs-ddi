---
UID : NF:ndis.NdisFSendNetBufferListsComplete
title : NdisFSendNetBufferListsComplete function
author : windows-driver-content
description : Filter drivers call the NdisFSendNetBufferListsComplete function to return a linked list of NET_BUFFER_LIST structures to an overlying driver and to return the final status of a send request.
old-location : netvista\ndisfsendnetbufferlistscomplete.htm
old-project : netvista
ms.assetid : 5a9008eb-86ad-4e3c-85a2-c8fd1b8fb4cb
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisFSendNetBufferListsComplete
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
req.alt-api : NdisFSendNetBufferListsComplete
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : Irql_Filter_Driver_Function
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


# NdisFSendNetBufferListsComplete function
Filter drivers call the 
  <b>NdisFSendNetBufferListsComplete</b> function to return a linked list of 
  <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structures to an overlying
  driver and to return the final status of a send request.

## Syntax

````
VOID NdisFSendNetBufferListsComplete(
  _In_ NDIS_HANDLE      NdisFilterHandle,
  _In_ PNET_BUFFER_LIST NetBufferLists,
  _In_ ULONG            SendCompleteFlags
);
````

## Parameters

`NdisFilterHandle`

The NDIS handle that identifies this filter module. NDIS passed the handle to the filter driver in
     a call to the 
     <a href="..\ndis\nc-ndis-filter_attach.md">FilterAttach</a> function.

`NetBufferList`



`SendCompleteFlags`

NDIS flags that can be combined with an OR operation. To clear all the flags, set this member to zero. This function supports the following flags:


## Return Value

None

## Remarks

A filter driver calls the 
    <b>NdisFSendNetBufferListsComplete</b> function to complete send requests that NDIS made to the driver's 
    <a href="..\ndis\nc-ndis-filter_send_net_buffer_lists.md">
    FilterSendNetBufferLists</a> function. The filter driver specifies a linked list of 
    <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structures that are
    associated with the completed send requests. While the status of the send requests is pending, the filter
    driver retains ownership of the <b>NET_BUFFER_LIST</b> structures and all the resources that are associated with
    the <b>NET_BUFFER_LIST</b> structures.

The filter driver can complete send requests in any order. For example, the filter driver could
    concatenate the <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structure lists from multiple 
    <a href="..\ndis\nc-ndis-filter_send_net_buffer_lists.md">FilterSendNetBufferLists</a> calls or split up a list from a 
    <i>FilterSendNetBufferLists</i> call. However, the filter driver must not modify the list of 
    <a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a> structures that are associated with a
    <b>NET_BUFFER_LIST</b> structure.

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
| **DDI compliance rules** | Irql_Filter_Driver_Function |

## See Also

<dl>
<dt>
<a href="..\ndis\nc-ndis-filter_attach.md">FilterAttach</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-filter_send_net_buffer_lists.md">FilterSendNetBufferLists</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisFSendNetBufferListsComplete function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>