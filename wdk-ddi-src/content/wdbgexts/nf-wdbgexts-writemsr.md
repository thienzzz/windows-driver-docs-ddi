---
UID : NF:wdbgexts.WriteMsr
title : WriteMsr function
author : windows-driver-content
description : The WriteMsr function writes to a Model-Specific Register (MSR).
old-location : debugger\writemsr.htm
old-project : debugger
ms.assetid : a88c2c74-ab9a-4d9a-aeb7-d08bfe497da4
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : WriteMsr
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdbgexts.h
req.include-header : Wdbgexts.h, Dbgeng.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WriteMsr
req.alt-loc : dbgeng.h
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
req.typenames : EXT_TDOP
req.product : Windows 10 or later.
---


# WriteMsr function
The <b>WriteMsr</b> function writes to a Model-Specific Register (MSR).

## Syntax

````
__inline VOID WriteMsr(
  _In_ ULONG   MsrReg,
  _In_ ULONG64 MsrValue
);
````

## Parameters

`MsrReg`

Specifies the ID number of the MSR.

`MsrValue`

Specifies the new value of the MSR.


## Return Value

None

## Remarks

For a WdbgExts extension, include wdbgexts.h. For a DbgEng extension, include wdbgexts.h before dbgeng.h. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff561480">Writing DbgEng Extension Code</a> for details.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdbgexts.h (include Wdbgexts.h, Dbgeng.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |