---
UID : NF:vmbuskernelmodeclientlibapi.VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT
title : VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT function
author : windows-driver-content
description : The VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT function saves callback functions to be used for state changes for a channel.
old-location : netvista\vmb_channel_state_change_callbacks_init.htm
old-project : netvista
ms.assetid : 2255C8A2-85FB-4B96-8AE9-66FAFD73EE73
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : vmbuskernelmodeclientlibapi.h
req.include-header : VmbusKernelModeClientLibApi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT
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


# VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT function
<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT</b> function saves callback functions to be used for state changes for a channel.

## Syntax

````
VOID WINAPI VMB_CHANNEL_STATE_CHANGE_CALLBACKS_INIT(
  _Out_ PVMB_CHANNEL_STATE_CHANGE_CALLBACKS Callbacks
);
````

## Parameters

`Callbacks`

A structure to save callback functions that relate to the state changes for a channel.


## Return Value

This function does not return a value.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | vmbuskernelmodeclientlibapi.h (include VmbusKernelModeClientLibApi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |