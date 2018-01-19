---
UID : NF:vmbuskernelmodeclientlibapi.VmbPacketSendWithExternalPfns
title : VmbPacketSendWithExternalPfns function
author : windows-driver-content
description : The VmbPacketSendWithExternalPfns function sends the data in a packet buffer or external data as an array of Page Frame Numbers (PFNs).
old-location : netvista\vmbpacketsendwithexternalpfns.htm
old-project : netvista
ms.assetid : 50AACCAB-EFEA-42B7-8A34-FE110C7CDEED
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : VmbPacketSendWithExternalPfns
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : vmbuskernelmodeclientlibapi.h
req.include-header : VmbusKernelModeClientLibApi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 1.13
req.umdf-ver : 2.0
req.alt-api : VmbPacketSendWithExternalPfns
req.alt-loc : VmbusKernelModeClientLibApi.h
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
req.typenames : "*PVIDEO_PORT_AGP_SERVICES, VIDEO_PORT_AGP_SERVICES"
req.product : Windows 10 or later.
---


# VmbPacketSendWithExternalPfns function
<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>VmbPacketSendWithExternalPfns</b> function sends the data in a packet buffer or external data as an array of Page Frame Numbers (PFNs). The function associates that data with the VMBus packet object, which represents the packet
throughout the lifetime of the transaction.

## Syntax

````
NTSTATUS VmbPacketSendWithExternalPfns(
  _In_ __drv_aliasesMem VMBPACKET       PacketObject,
  _In_ reads_bytes_(BufferLength) PVOID Buffer,
  _In_ UINT32                           BufferLength,
  _In_ PPFN_NUMBER                      ExternalDataPfns,
  _In_ UINT32                           PfnOffset,
  _In_ UINT32                           PfnLength,
  _In_ UINT32                           Flags
);
````

## Parameters

`PacketObject`

A handle to the VMBus packet object.

`Buffer`

A buffer that contains the command packet that is sent
through the VMBus ring buffer.

`BufferLength`

The length, in bytes, of the buffer in the <i>Buffer</i> parameter.

`ExternalDataPfns`

An array of Page Frame 
Numbers that describe a data buffer associated with 
the packet.

`PfnLength`

The number of PFNs to send from 
<i>ExternalDataPfns</i>. The final referenced array index is  ExternalDataPfns[PfnOffset+PfnLength-1] inclusive.

`Flags`

Flags. The following are pertinent flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>


## Return Value

<b>VmbPacketSendWithExternalPfns</b> returns a status code.

## Remarks

This function differs from the <a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketsend.md">VmbPacketSend</a> function in that it allows passing an array of PFNs,  effectively physical addresses.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** | 1.13 |
| **Minimum UMDF version** | 2.0 |
| **Header** | vmbuskernelmodeclientlibapi.h (include VmbusKernelModeClientLibApi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbpacketsend.md">VmbPacketSend</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20VmbPacketSendWithExternalPfns function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>