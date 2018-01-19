---
UID : NF:vmbuskernelmodeclientlibapi.VmbClientChannelInitSetRingBufferPageCount
title : VmbClientChannelInitSetRingBufferPageCount function
author : windows-driver-content
description : The VmbClientChannelInitSetRingBufferPageCount function sets the number of pages of memory the client allocates for incoming and outgoing ring buffers.
old-location : netvista\vmbclientchannelinitsetringbufferpagecount.htm
old-project : netvista
ms.assetid : 560A7CD9-5D9D-434B-ACEE-5852CC9A2CC3
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : VmbClientChannelInitSetRingBufferPageCount
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
req.alt-api : VmbClientChannelInitSetRingBufferPageCount
req.alt-loc : vmbkmcl.lib,vmbkmcl.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Vmbkmcl.lib
req.dll : 
req.irql : 
req.typenames : "*PVIDEO_PORT_AGP_SERVICES, VIDEO_PORT_AGP_SERVICES"
req.product : Windows 10 or later.
---


# VmbClientChannelInitSetRingBufferPageCount function
<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>VmbClientChannelInitSetRingBufferPageCount</b> function sets the number of pages of memory the client allocates for incoming and outgoing ring
buffers.

## Syntax

````
NTSTATUS
 VmbClientChannelInitSetRingBufferPageCount(
  _In_     VMBCHANNEL Channel,
  _In_ UINT32         IncomingPageCount,
  _In_ UINT32         OutgoingPageCount
);
````

## Parameters

`Channel`

A handle for a channel.

`IncomingPageCount`

Number of pages to allocate for the incoming ring     buffer.

`OutgoingPageCount`

Number of pages to allocate for the outgoing ring
buffer.


## Return Value

None

## Remarks

Because the client virtual machine donates the pages for both the incoming and the outgoing ring
buffers, this function can only be invoked on the client endpoint.</p>

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