---
UID : NF:wdm.READ_REGISTER_ULONG
title : READ_REGISTER_ULONG function
author : windows-driver-content
description : The READ_REGISTER_ULONG routine reads a ULONG value from the specified register address.
old-location : kernel\read_register_ulong.htm
old-project : kernel
ms.assetid : a462734c-cac6-4de0-95c1-810766ef1644
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : READ_REGISTER_ULONG
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
req.alt-api : READ_REGISTER_ULONG
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


# READ_REGISTER_ULONG function
The <b>READ_REGISTER_ULONG</b> routine reads a ULONG value from the specified register address.

## Syntax

````
ULONG READ_REGISTER_ULONG(
  _In_ PULONG Register
);
````

## Parameters

`Register`

Pointer to the register address, which must be a mapped range in memory space.


## Return Value

<b>READ_REGISTER_ULONG</b> returns the ULONG value read from the specified register address.

## Remarks

Callers of <b>READ_REGISTER_ULONG</b> can be running at any IRQL, assuming the <i>Register</i> is resident, mapped device memory.</p>

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