---
UID : NF:dbgeng.IDebugSystemObjects2.GetCurrentProcessHandle
title : IDebugSystemObjects2::GetCurrentProcessHandle method
author : windows-driver-content
description : The GetCurrentProcessHandle function returns the system handle for the current process.
old-location : debugger\getcurrentprocesshandle.htm
old-project : debugger
ms.assetid : b6780f1c-e093-4d91-8909-dabb1ecaefaa
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugSystemObjects2, IDebugSystemObjects2::GetCurrentProcessHandle, GetCurrentProcessHandle
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : dbgeng.h
req.include-header : Wdbgexts.h, Dbgeng.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : GetCurrentProcessHandle
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
req.typenames : "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---


# GetCurrentProcessHandle method
The <b>GetCurrentProcessHandle</b> function returns the system handle for the current process.

## Syntax

````
__inline VOID GetCurrentProcessHandle(
   PHANDLE hp
);
````

## Parameters

`Handle`




## Return Value

None

## Remarks

In kernel-mode debugging, the only process in the target is the virtual process created for the kernel. In this case, an artificial handle is created. The artificial handle can only be used with the debugger.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Wdbgexts.h, Dbgeng.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |