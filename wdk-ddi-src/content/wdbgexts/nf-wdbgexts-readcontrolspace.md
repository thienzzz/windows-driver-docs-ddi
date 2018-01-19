---
UID : NF:wdbgexts.ReadControlSpace
title : ReadControlSpace function
author : windows-driver-content
description : The ReadControlSpace function reads the processor-specific control space into the array pointed to by buf.
old-location : debugger\readcontrolspace.htm
old-project : debugger
ms.assetid : 4b6955a5-ca03-418d-9eba-fdbe48599922
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : ReadControlSpace
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
req.alt-api : ReadControlSpace
req.alt-loc : wdbgexts.h
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


# ReadControlSpace function
The <b>ReadControlSpace</b> function reads the processor-specific control space into the array pointed to by <i>buf</i>.

## Syntax

````
__inline VOID ReadControlSpace(
   USHORT processor,
   ULONG  address,
   PVOID  buf,
   ULONG  size
);
````

## Parameters

`processor`

Specifies the number of the processor whose control space is to be read.

`address`

Specifies the address of the control space.

`buf`

Specifies the address of an array of bytes to hold the control space data.

`size`

Specifies the number of bytes in the array pointed to by <i>buf</i>.


## Return Value

None

## Remarks

If you are writing 64-bit code, you should use <a href="..\wdbgexts\ns-wdbgexts-_readcontrolspace64.md">ReadControlSpace64</a> instead. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff537780">32-Bit Pointers and 64-Bit Pointers</a> for details.

If you are writing a WdbgExts extension, include <b>wdbgexts.h</b>. If you are writing a DbgEng extension that calls this function, include <b>wdbgexts.h</b> before <b>dbgeng.h</b> (see <a href="https://msdn.microsoft.com/library/windows/hardware/ff561480">Writing DbgEng Extension Code</a> for details).
</p>

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