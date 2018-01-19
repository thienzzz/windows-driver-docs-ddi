---
UID : NF:vmbuskernelmodeclientlibapi.VmbChannelInitSetStateChangeCallbacks
title : VmbChannelInitSetStateChangeCallbacks function
author : windows-driver-content
description : The VmbChannelInitSetStateChangeCallbacks function sets optional callback functions for state changes.
old-location : netvista\vmbchannelinitsetstatechangecallbacks.htm
old-project : netvista
ms.assetid : 4E6088EA-7081-4B80-8F83-15B39A0F30AB
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : VmbChannelInitSetStateChangeCallbacks
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
req.alt-api : VmbChannelInitSetStateChangeCallbacks
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


# VmbChannelInitSetStateChangeCallbacks function
<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>VmbChannelInitSetStateChangeCallbacks</b>  function sets optional callback functions for state changes.

## Syntax

````
NTSTATUS VmbChannelInitSetStateChangeCallbacks(
  _In_ VMBCHANNEL                          Channel,
  _In_ PVMB_CHANNEL_STATE_CHANGE_CALLBACKS StateChangeCallbacks
);
````

## Parameters

`Channel`

A handle for a channel.

`StateChangeCallbacks`

A structure of state change callbacks to set.


## Return Value

<b>VmbChannelInitSetStateChangeCallbacks</b> returns one of the following status values: 
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The function finished successfully.
<dl>
<dt><b>STATUS_INVALID_PARAMETER_1</b></dt>
</dl>The <i>Channel</i> value was invalid or in an invalid state, such as Disabled.
<dl>
<dt><b>STATUS_INVALID_PARAMETER_2</b></dt>
</dl>The <i>StateChangeCallbacks</i> value is the wrong version or size.


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