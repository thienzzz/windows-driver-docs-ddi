---
UID : NF:wdfhwaccess.WDF_READ_PORT_BUFFER_UCHAR
title : WDF_READ_PORT_BUFFER_UCHAR function
author : windows-driver-content
description : The WDF_READ_PORT_BUFFER_UCHAR function reads a number of bytes from the specified port address into a buffer.
old-location : wdf\wdf_read_port_buffer_uchar.htm
old-project : wdf
ms.assetid : 1A205DD3-FCE2-4EA1-A6B3-CE60300EC651
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WDF_READ_PORT_BUFFER_UCHAR
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfhwaccess.h
req.include-header : 
req.target-type : Universal
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 2.0
req.alt-api : WDF_READ_PORT_BUFFER_UCHAR
req.alt-loc : Wdfhwaccess.h
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
req.typenames : WDF_FILE_INFORMATION_CLASS, *PWDF_FILE_INFORMATION_CLASS
req.product : Windows 10 or later.
---


# WDF_READ_PORT_BUFFER_UCHAR function
<p class="CCE_Message">[Applies to UMDF only]

The <b>WDF_READ_PORT_BUFFER_UCHAR</b> function reads a number of bytes from the specified port address into a buffer.

## Syntax

````
void WDF_READ_PORT_BUFFER_UCHAR(
  _In_  WDFDEVICE Device,
  _In_  PUCHAR    Port,
  _Out_ PUCHAR    Buffer,
  _In_  ULONG     Count 
);
````

## Parameters

`Device`

A handle to a framework device object.

`Port`

Specifies the port address, which must be a mapped memory range in I/O space.

`Buffer`

A pointer to a buffer into which an array of UCHAR values is read.

`Count`

Specifies the number of bytes to be read into the buffer.


## Return Value

This function does not return a value.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfhwaccess.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |