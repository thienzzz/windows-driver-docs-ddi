---
UID : NC:ndis.NDIS_SWITCH_ALLOCATE_NET_BUFFER_LIST_FORWARDING_CONTEXT
title : NDIS_SWITCH_ALLOCATE_NET_BUFFER_LIST_FORWARDING_CONTEXT
author : windows-driver-content
description : The AllocateNetBufferListForwardingContext function prepares a NET_BUFFER_LIST structure for send or receive operations within the extensible switch.
old-location : netvista\AllocateNetBufferListForwardingContext.htm
old-project : netvista
ms.assetid : C8A80DB2-4273-4FBA-82D4-4E8146812B16
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RxNameCacheInitialize
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Desktop
req.target-min-winverclnt : Supported in NDIS 6.30 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : AllocateNetBufferListForwardingContext
req.alt-loc : Ndis.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : VIDEO_STREAM_INIT_PARMS, *LPVIDEO_STREAM_INIT_PARMS
---


# NDIS_SWITCH_ALLOCATE_NET_BUFFER_LIST_FORWARDING_CONTEXT function
The <i>AllocateNetBufferListForwardingContext</i> function prepares a <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structure for send or receive operations within the extensible switch.



The <i>AllocateNetBufferListForwardingContext</i> function prepares a <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structure for send or receive operations within the extensible switch.

## Syntax

```
NDIS_SWITCH_ALLOCATE_NET_BUFFER_LIST_FORWARDING_CONTEXT NdisSwitchAllocateNetBufferListForwardingContext;

NDIS_STATUS NdisSwitchAllocateNetBufferListForwardingContext(
  NDIS_SWITCH_CONTEXT NdisSwitchContext,
  PNET_BUFFER_LIST NetBufferList
)
{...}
```

## Parameters

`NdisSwitchContext`

An NDIS_SWITCH_CONTEXT value that contains the handle of the extensible switch module to which the Hyper-V extensible switch extension is attached. When the extension calls <a href="..\ndis\nf-ndis-ndisfgetoptionalswitchhandlers.md">NdisFGetOptionalSwitchHandlers</a>,  this handle is returned through the <i>NdisSwitchContext</i> parameter.

`NetBufferList`

A pointer to a linked list of <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structures.


## Return Value

If the call succeeds, the function returns NDIS_STATUS_SUCCESS. Otherwise, it returns an NDIS_STATUS_<i>Xxx</i> error code that is defined in Ndis.h.

## Remarks

The extensible switch extension can originate packet send operations within the extensible switch data path. For example, the extension can send packets to any port on the extensible switch. For more information about this data path, see <a href="https://msdn.microsoft.com/5E7F135B-3086-415F-8D39-98CDBED8EBB4">Hyper-V Extensible Switch Data Path</a>.

After the extension calls <a href="..\ndis\nf-ndis-ndisallocatenetbufferlist.md">NdisAllocateNetBufferList</a> or <a href="..\ndis\nf-ndis-ndisallocateclonenetbufferlist.md">NdisAllocateCloneNetBufferList</a> to create or clone a packet from its <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> pool, the extension must  call the <i>AllocateNetBufferListForwardingContext</i> function. This function allocates and initializes the out-of-band (OOB) extensible switch forwarding context for the specified  <b>NET_BUFFER_LIST</b> structure. For more information about this context, see <a href="https://msdn.microsoft.com/B2BF07B5-FA44-4994-9605-EFF4A0B9179F">Hyper-V Extensible Switch Forwarding Context</a>.

The extension must follow these guidelines for allocating the forwarding context through the <i>AllocateNetBufferListForwardingContext</i> function:

The extension calls <a href="..\ndis\nf-ndis-ndisallocatenetbufferlist.md">NdisAllocateNetBufferList</a> to allocate a packet from the extension's <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> pool for a send or receive operation over the extensible switch. Before the extension initializes source and destination ports for the packet, it must call <i>AllocateNetBufferListForwardingContext</i>. 

For more information on how to specify source and destination extensible switch ports, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/managing-hyper-v-extensible-switch-source-and-destination-port-data">Managing Hyper-V Extensible Switch Source and Destination Port Data</a>.

Before the extension calls <i>AllocateNetBufferListForwardingContext</i>, it must set the <b>SourceHandle</b> member of each allocated <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structure to the handle value that identifies the extension. The extension receives this handle through the <i>NdisFilterHandle</i> parameter when NDIS calls the extension's <a href="..\ndis\nc-ndis-filter_attach.md">FilterAttach</a> function.

When the send operation is complete, the extension must call the <a href="https://msdn.microsoft.com/08AE3160-276F-4D1F-9D02-AD5AF38CDED2">FreeNetBufferListForwardingContext</a> function to deallocate the resources for the forwarding context. The extension must call this function before it calls <a href="..\ndis\nf-ndis-ndisfreenetbufferlist.md">NdisFreeNetBufferList</a> to return the packet to its <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> pool.

If the extension is cloning a packet, it must call <a href="https://msdn.microsoft.com/5CC345FA-C3EF-4122-8E9C-6EA27B20DD5A">CopyNetBufferListInfo</a> to copy the forwarding context from the original packet to the cloned packet. The extension must do this after it calls <i>AllocateNetBufferListForwardingContext</i>.

 For more information on how to originate send operations, see <a href="https://msdn.microsoft.com/208f9af6-cde4-4801-9355-daa6633d7d0b">Filter Module Send and Receive Operations</a>.

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
| **DDI compliance rules** |  |

## See Also

<dl>
<dt><b></b></dt>
<dt>
<a href="https://msdn.microsoft.com/5CC345FA-C3EF-4122-8E9C-6EA27B20DD5A">CopyNetBufferListInfo</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-filter_attach.md">FilterAttach</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/08AE3160-276F-4D1F-9D02-AD5AF38CDED2">FreeNetBufferListForwardingContext</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisallocatenetbufferlist.md">NdisAllocateNetBufferList</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisfgetoptionalswitchhandlers.md">NdisFGetOptionalSwitchHandlers</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisfreenetbufferlist.md">NdisFreeNetBufferList</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_SWITCH_ALLOCATE_NET_BUFFER_LIST_FORWARDING_CONTEXT callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>