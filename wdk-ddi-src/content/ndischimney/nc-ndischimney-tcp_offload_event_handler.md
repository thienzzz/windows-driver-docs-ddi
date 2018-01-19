---
UID : NC:ndischimney.TCP_OFFLOAD_EVENT_HANDLER
title : TCP_OFFLOAD_EVENT_HANDLER
author : windows-driver-content
description : NDIS calls a protocol driver's or intermediate driver's ProtocolIndicateOffloadEvent function to post an indication that was initiated by an underlying driver's or offload target's call to the NdisTcpOffloadEventHandler function.
old-location : netvista\protocoltcpoffloadevent.htm
old-project : netvista
ms.assetid : b64c0f9e-aa3d-43c5-bdf5-c40cae3929e3
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _PD_BUFFER_VIRTUAL_SUBNET_INFO, PD_BUFFER_VIRTUAL_SUBNET_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : ndischimney.h
req.include-header : Ndischimney.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ProtocolTcpOffloadEvent
req.alt-loc : Ndischimney.h
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
req.typenames : PD_BUFFER_VIRTUAL_SUBNET_INFO
---


# TCP_OFFLOAD_EVENT_HANDLER callback function
<p class="CCE_Message">[The TCP chimney offload feature is deprecated and should not be used.]

NDIS calls a protocol driver's or intermediate driver's 
  <i>ProtocolIndicateOffloadEvent</i> function to post an indication that was initiated by an underlying
  driver's or offload target's call to the 
  <a href="..\ndischimney\nc-ndischimney-ndis_tcp_offload_event_indicate.md">
  NdisTcpOffloadEventHandler</a> function.

## Syntax

```
TCP_OFFLOAD_EVENT_HANDLER TcpOffloadEventHandler;

void TcpOffloadEventHandler(
  IN PVOID OffloadContext,
  IN ULONG EventType,
  IN ULONG EventSpecificInformation
)
{...}
```

## Parameters

`OffloadContext`

A pointer to the protocol or intermediate driver's 
     <a href="..\ndischimney\ns-ndischimney-_ndis_offload_handle.md">NDIS_OFFLOAD_HANDLE</a> structure for the
     TCP connection on which the indication is being made. The protocol or intermediate driver supplied this
     pointer as an input parameter to the 
     <a href="..\ndischimney\nf-ndischimney-ndisinitiateoffload.md">NdisInitiateOffload</a> function when
     offloading the connection.

`EventType`

The event being indicated as one of the following TCP_OFFLOAD_EVENT_TYPE values:

`EventSpecificInformation`

Specifies additional information about the event being indicated as follows:


## Return Value

None

## Remarks

To propagate the indication to the overlying driver or host stack, the intermediate driver calls the 
    <b>NdisTcpOffloadEventHandler</b> function. The intermediate driver passes the following parameters to the
    
    <b>NdisTcpOffloadEventHandler</b> function:

The 
      <b>NdisOffloadHandle</b> that the offload target stored in its context for the offloaded TCP connection.
      For more information, see 
      <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/referencing-offloaded-state-through-an-intermediate-driver">
      Referencing Offloaded State Through an Intermediate Driver</a>.

The 
      <i>EventType</i> that NDIS passed to the intermediate driver's 
      <i>ProtocolTcpOffloadEvent</i> function.

The 
      <i>EventSpecificInformation</i> that NDIS passed to the intermediate driver's 
      <i>ProtocolTcpOffloadEvent</i> function.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndischimney.h (include Ndischimney.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ndischimney\nc-ndischimney-ndis_tcp_offload_event_indicate.md">NdisTcpOffloadEventHandler</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20TCP_OFFLOAD_EVENT_HANDLER callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>