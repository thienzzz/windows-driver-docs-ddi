---
UID : NF:wdm.READ_REGISTER_BUFFER_USHORT
title : READ_REGISTER_BUFFER_USHORT function
author : windows-driver-content
description : The READ_REGISTER_BUFFER_USHORT routine reads a number of USHORT values from the specified register address into a buffer.
old-location : kernel\read_register_buffer_ushort.htm
old-project : kernel
ms.assetid : 30c3fc44-e94a-47ca-a25b-33857b485817
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : READ_REGISTER_BUFFER_USHORT
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
req.alt-api : READ_REGISTER_BUFFER_USHORT
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : Any level (see Remarks section)
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# READ_REGISTER_BUFFER_USHORT function
The <b>READ_REGISTER_BUFFER_USHORT</b> routine reads a number of USHORT values from the specified register address into a buffer.

## Syntax

````
VOID READ_REGISTER_BUFFER_USHORT(
  _In_  PUSHORT Register,
  _Out_ PUSHORT Buffer,
  _In_  ULONG   Count
);
````

## Parameters

`Register`

Pointer to the register, which must be a mapped range in memory space.

`Buffer`

Pointer to a buffer into which an array of USHORT values is read.

`Count`

Specifies the number of USHORT values to be read into the buffer.


## Return Value

None

## Remarks

The size of the buffer must be large enough to contain at least the specified number of USHORT values.

Callers of <b>READ_REGISTER_BUFFER_USHORT</b> can be running at any IRQL, assuming the <i>Buffer</i> is resident and the <i>Register</i> is resident, mapped device memory.</p>

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