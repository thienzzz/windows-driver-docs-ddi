---
UID : NS:ndischimney._NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST
title : _NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST
author : windows-driver-content
description : The NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure.
old-location : netvista\ndis_protocol_offload_block_list.htm
old-project : netvista
ms.assetid : 64febd55-1ab8-4e2e-b738-340167866333
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST, *PNDIS_PROTOCOL_OFFLOAD_BLOCK_LIST, NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ndischimney.h
req.include-header : Ndischimney.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST
req.alt-loc : ndischimney.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : "*PNDIS_PROTOCOL_OFFLOAD_BLOCK_LIST, NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST"
---

# _NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure
<p class="CCE_Message">[The TCP chimney offload feature is deprecated and should not be used.]

The NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure.

## Syntax
````
typedef struct _NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST {
  NDIS_OBJECT_HEADER                       Header;
  struct _NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST  *NextBlock;
  struct _NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST  *DependentBlockList;
  NDIS_STATUS                              Status;
  PVOID                                    NdisReserved[3];
  PNDIS_OFFLOAD_HANDLE                     OffloadHandle;
  PVOID                                    ProtocolReserved[2];
  PVOID                                    MiniportReserved[2];
  PVOID                                    ImReserved[2];
  PVOID                                    Scratch[2];
  PVOID                                    SourceHandle;
  NDIS_PORT_NUMBER                         PortNumber;
  PNET_BUFFER_LIST                         NetBufferListChain;
} NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST, *PNDIS_PROTOCOL_OFFLOAD_BLOCK_LIST;
````

## Members

        
            `DependentBlockList`

            A pointer to an NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure that is at a dependent layer of the
     offload state (a higher layer in the offload state tree).
        
            `Header`

            The header of the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure. The header is formatted as an 
     <a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a> structure. The
     NDIS_OBJECT_HEADER structure contains the revision number of the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST
     structure, the type of offload state that immediately follows the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST
     structure in memory, and the size of the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure, including the
     header, in bytes. 
     

The 
     <b>Type</b> member of the NDIS_OBJECT_HEADER structure indicates the type of offload state, and by
     implication, the specific offload state structure (or structures) that immediately follow the
     NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure in memory.

The following OFFLOAD_STATE_TYPE values are supported:
        
            `ImReserved`

            Reserved for use by intermediate drivers, which can use this area for their own purposes.
        
            `MiniportReserved`

            Reserved for use by offload targets or the miniport portion of an intermediate driver.
        
            `NdisReserved`

            Reserved for use by NDIS.
        
            `NetBufferListChain`

            When the protocol or intermediate driver specifies a <b>NULL</b> value, 
      <b>NetBufferListChain</b> is not significant and can be ignored by the underlying driver or offload
      target.

When a protocol or intermediate driver specifies a non-<b>NULL</b> value, 
      <b>NetBufferListChain</b> points to a 
      <a href="..\ndis\ns-ndis-_net_buffer_list.md">NET_BUFFER_LIST</a> structure that can be a
      stand-alone structure or the first structure in a linked list of such structures. Each NET_BUFFER_LIST
      structure in the linked list describes one 
      <a href="..\ndis\ns-ndis-_net_buffer.md">NET_BUFFER</a> structure. The NET_BUFFER structure
      maps to a chain of memory descriptor lists (MDLs). The NET_BUFFER_LIST and associated structures are
      locked so that they remain resident in physical memory. However, they are not mapped into system
      memory.

The MDLs associated with the NET_BUFFER structures contain data that is being conveyed as part of a
      state-manipulation operation or the completion of such an operation. At present, the linked list can
      contain just one type of data: outstanding send data. For more information about send data, see 
      <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/handling-outstanding-send-data-during-and-after-an-offload-operation">Handling
      Outstanding Send Data During and After an Offload Operation</a>.

An offload target or intermediate driver can pass outstanding send data to the overlying driver or
      host stack when terminating the offload of a TCP connection. In this case, the offload target specifies
      a non-<b>NULL</b> value for the 
      <b>NetBufferListChain</b> member when calling the 
      <a href="..\ndischimney\nf-ndischimney-ndismterminateoffloadcomplete.md">
      NdisMTerminateOffloadComplete</a> function. If the offload target is not passing send data for a TCP
      connection that is being terminated, it specifies a <b>NULL</b> value for the 
      <b>NetBufferListChain</b> member.
        
            `NextBlock`

            A pointer to the next NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure at the offload state layer
     (neighbor, path, or TCP) indicated by the 
     <b>Type</b> member of the 
     <b>Header</b> member. NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structures that are linked through 
     <b>NextBlock</b> pointers are always at the same layer of the offload state. A 
     <b>NextBlock</b> value of <b>NULL</b> indicates that there is no additional next
     NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure at this level.
        
            `OffloadHandle`

            A pointer to an 
     <a href="..\ndischimney\ns-ndischimney-_ndis_offload_handle.md">NDIS_OFFLOAD_HANDLE</a> structure. The
     NDIS_OFFLOAD_HANDLE structure represents a protocol or intermediate driver's context for an offloaded
     state object.
        
            `PortNumber`

            A port number that identifies a miniport adapter port. To assign a miniport adapter port number,
     call the 
     <a href="..\ndis\nf-ndis-ndismallocateport.md">NdisMAllocatePort</a> function. A zero
     value identifies the default port of a miniport adapter. Use the default port if the miniport driver has
     not allocated ports for the specified adapter.
        
            `ProtocolReserved`

            Reserved for use by protocol drivers, which can use this area for their own purposes.
        
            `Scratch`

            The protocol driver or intermediate driver can use this area for internal tracking. The
     information in this area is valid only while the driver has ownership of the 
     <b>
     NDIS_PROTOCOL_OFFLOAD_BLOCK_LIS</b> T.
        
            `SourceHandle`

            This member is not significant for a protocol or intermediate driver. A protocol or intermediate
      driver must not modify this member.

When propagating the completion of a state-manipulation operation, an intermediate driver copies the
      
      <b>SourceHandle</b> that it stored in its IM call entry to the 
      <b>SourceHandle</b> member of the 
      <a href="..\ndischimney\ns-ndischimney-_ndis_miniport_offload_block_list.md">
      NDIS_MINIPORT_OFFLOAD_BLOCK_LIST</a> structure that it passes to the NdisMXxxComplete function.
        
            `Status`

            The completion status of an initiate offload, query offload, update offload, invalidate offload,
     or terminate offload operation that the offload target performed on the state associated with, or
     referenced by, the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure. Depending on the operation, NDIS writes
     one of the following NDIS_STATUS values to the 
     <b>Status</b> member:

    ## Remarks
        An intermediate driver creates an NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure from an 
    <a href="..\ndischimney\ns-ndischimney-_ndis_miniport_offload_block_list.md">
    NDIS_MINIPORT_OFFLOAD_BLOCK_LIST</a> structure when 
    <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff563771">propagating a
    state-manipulation operation</a>. When 
    <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/propagating-the-completion-of-a-state-manipulation-operation">
    propagating the completion of such an operation</a>, an intermediate driver uses an
    NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure to construct an NDIS_MINIPORT_OFFLOAD_BLOCK_LIST
    structure.

An NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure can be immediately followed in memory by an 
    <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff570939">offload state structure</a> that contains
    the state to be (or that has been) offloaded, queried, updated, invalidated, or terminated. The 
    <b>Type</b> member of the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure's 
    <b>Header</b> specifies the type of offload state, and by implication, the specific offload state
    structure (or structures) that follow the NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure in memory.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndischimney.h (include Ndischimney.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ndischimney\nf-ndischimney-ndisinitiateoffload.md">NdisInitiateOffload</a>
</dt>
<dt>
<a href="..\ndischimney\nf-ndischimney-ndisinvalidateoffload.md">NdisInvalidateOffload</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismallocateport.md">NdisMAllocatePort</a>
</dt>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a>
</dt>
<dt>
<a href="..\ndischimney\nf-ndischimney-ndisqueryoffloadstate.md">NdisQueryOffload</a>
</dt>
<dt>
<a href="..\ndischimney\nf-ndischimney-ndisterminateoffload.md">NdisTerminateOffload</a>
</dt>
<dt>
<a href="..\ndischimney\nf-ndischimney-ndisupdateoffload.md">NdisUpdateOffload</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_neighbor_offload_state_cached.md">NEIGHBOR_OFFLOAD_STATE_CACHED</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_neighbor_offload_state_const.md">NEIGHBOR_OFFLOAD_STATE_CONST</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_neighbor_offload_state_delegated.md">
   NEIGHBOR_OFFLOAD_STATE_DELEGATED</a>
</dt>
<dt>
<a href="..\ndischimney\nc-ndischimney-initiate_offload_complete_handler.md">
   ProtocolInitiateOffloadComplete</a>
</dt>
<dt>
<a href="..\ndischimney\nc-ndischimney-invalidate_offload_complete_handler.md">
   ProtocolInvalidateOffloadComplete</a>
</dt>
<dt>
<a href="..\ndischimney\nc-ndischimney-query_offload_complete_handler.md">
   ProtocolQueryOffloadComplete</a>
</dt>
<dt>
<a href="..\ndischimney\nc-ndischimney-terminate_offload_complete_handler.md">
   ProtocolTerminateOffloadComplete</a>
</dt>
<dt>
<a href="..\ndischimney\nc-ndischimney-update_offload_complete_handler.md">
   ProtocolUpdateOffloadComplete</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_path_offload_state_cached.md">PATH_OFFLOAD_STATE_CACHED</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_path_offload_state_const.md">PATH_OFFLOAD_STATE_CONST</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_path_offload_state_delegated.md">PATH_OFFLOAD_STATE_DELEGATED</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_tcp_offload_state_cached.md">TCP_OFFLOAD_STATE_CACHED</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_tcp_offload_state_const.md">TCP_OFFLOAD_STATE_CONST</a>
</dt>
<dt>
<a href="..\ndischimney\ns-ndischimney-_tcp_offload_state_delegated.md">TCP_OFFLOAD_STATE_DELEGATED</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_PROTOCOL_OFFLOAD_BLOCK_LIST structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>