---
UID : NF:wdm.READ_PORT_BUFFER_ULONG
title : READ_PORT_BUFFER_ULONG function
author : windows-driver-content
description : The READ_PORT_BUFFER_ULONG routine reads a number of ULONG values from the specified port address into a buffer.
old-location : kernel\read_port_buffer_ulong.htm
old-project : kernel
ms.assetid : a63028d8-f90e-4f86-81f5-27bc727ecad7
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : READ_PORT_BUFFER_ULONG
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : READ_PORT_BUFFER_ULONG
req.alt-loc : Hal.lib,Hal.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Hal.lib
req.dll : 
req.irql : Any level (see Remarks section)
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# READ_PORT_BUFFER_ULONG function
The <b>READ_PORT_BUFFER_ULONG</b> routine reads a number of ULONG values from the specified port address into a buffer.

## Syntax

````
VOID READ_PORT_BUFFER_ULONG(
  _In_  PULONG Port,
  _Out_ PULONG Buffer,
  _In_  ULONG  Count
);
````

## Parameters

`Port`

Specifies the port address, which must be a mapped memory range in I/O space.

`Buffer`

Pointer to a buffer into which an array of ULONG values is read.

`Count`

Specifies the number of ULONG values to be read into the buffer.


## Return Value

None

## Remarks

The size of the buffer must be large enough to contain at least the specified number of ULONG values.

Callers of <b>READ_PORT_BUFFER_ULONG</b> can be running at any IRQL, assuming the <i>Buffer</i> is resident and the <i>Port</i> is resident, mapped device memory.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | Any level (see Remarks section) |
| **DDI compliance rules** |  |