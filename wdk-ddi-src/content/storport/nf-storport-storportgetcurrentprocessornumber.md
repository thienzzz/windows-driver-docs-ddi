---
UID : NF:storport.StorPortGetCurrentProcessorNumber
title : StorPortGetCurrentProcessorNumber function
author : windows-driver-content
description : The StorPortGetCurrentProcessorNumber routine retrieves the current processor number from the kernel.
old-location : storage\storportgetcurrentprocessornumber.htm
old-project : storage
ms.assetid : 10d77823-fcaa-43c3-b55e-74f2da97ecf0
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortGetCurrentProcessorNumber
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 7.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortGetCurrentProcessorNumber
req.alt-loc : storport.h
req.ddi-compliance : StorPortIrql
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortGetCurrentProcessorNumber function
The <b>StorPortGetCurrentProcessorNumber</b> routine retrieves the current processor number from the kernel.

## Syntax

````
ULONG StorPortGetCurrentProcessorNumber(
  _In_  PVOID             HwDeviceExtension,
  _Out_ PPROCESSOR_NUMBER ProcNumber
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension for the host bus adapter (HBA).

`ProcNumber`

A pointer to a processor number structure that holds the return data.


## Return Value

The <b>StorPortGetCurrentProcessorNumber</b> routine returns one of the following status codes:
<dl>
<dt><b>STOR_STATUS_NOT_IMPLEMENTED</b></dt>
</dl>This function is not implemented on the active operating system.
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>The operation was successful.
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl>The operation fails with this return value if one or more of the parameters are invalid, for example, if <i>ProcNumber</i> is set to <b>NULL</b>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** | StorPortIrql |