---
UID : NF:wdbgexts.ReadIoSpaceEx64
title : ReadIoSpaceEx64 function
author : windows-driver-content
description : The ReadIoSpaceEx64 function is an extended version of ReadIoSpace64.
old-location : debugger\readiospaceex64.htm
old-project : debugger
ms.assetid : 6903a684-e9da-4ff0-b5ea-330b070849c6
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : ReadIoSpaceEx64
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
req.alt-api : ReadIoSpaceEx64
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


# ReadIoSpaceEx64 function
The <b>ReadIoSpaceEx64</b> function is an extended version of <a href="..\wdbgexts\nf-wdbgexts-readiospace64.md">ReadIoSpace64</a>. It reads not only the system I/O locations, but also I/O locations on a bus. <b>ReadIoSpace64</b> works like <b>ReadIoSpaceEx64</b>, except that it defaults <i>interfacetype</i> to ISA, <i>busnumber</i> to zero, and <i>addressspace</i> to 1.

## Syntax

````
__inline VOID ReadIoSpaceEx64(
   ULONG64 address,
   PULONG  data,
   PULONG  size,
   ULONG   interfacetype,
   ULONG   busnumber,
   ULONG   addressspace
);
````

## Parameters

`address`

Specifies the I/O address to read from.

`data`

Specifies the address of a variable to hold the data read. This must be at least the number of bytes contained in <i>size</i>.

`size`

Specifies the address of a variable that contains the number of bytes to read. <i>Size</i> must be 1, 2, or 4. After the data is read, <i>size</i> will contain the number of bytes actually read.

`interfacetype`

Specifies the type of interface on which the extended I/O space exists. Possible values include ISA, EISA, and MCA. For more information, see ntddk.h, which is available as part of Windows Driver Kit.

`busnumber`

Specifies the number of the bus on which the extended I/O space exists. This is typically zero, unless there is more than one bus of a given type.

`addressspace`

This is typically 1.


## Return Value

None

## Remarks

If you are writing 32-bit code, you should use <a href="..\wdbgexts\nf-wdbgexts-readiospaceex.md">ReadIoSpaceEx</a> instead. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff537780">32-Bit Pointers and 64-Bit Pointers</a> for details.

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