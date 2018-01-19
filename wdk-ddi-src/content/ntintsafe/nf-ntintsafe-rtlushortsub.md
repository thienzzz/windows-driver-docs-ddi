---
UID : NF:ntintsafe.RtlUShortSub
title : RtlUShortSub function
author : windows-driver-content
description : Subtracts one value of type USHORT from another.
old-location : kernel\rtlushortsub.htm
old-project : kernel
ms.assetid : 1C0392AE-F3BD-4F42-9094-87228B7C3E10
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlUShortSub
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntintsafe.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlUShortSub
req.alt-loc : Ntintsafe.h
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
req.typenames : PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION
---


# RtlUShortSub function
Subtracts one value of type <b>USHORT</b> from another.

## Syntax

````
NTSTATUS RtlUShortSub(
  _In_  USHORT usMinuend,
  _In_  USHORT usSubtrahend,
  _Out_ USHORT *pusResult
);
````

## Parameters

`usMinuend`

The value from which <i>usSubtrahend</i> is subtracted.

`usSubtrahend`

The value to subtract from <i>usMinuend</i>.

`pusResult`

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## Return Value

None

## Remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntintsafe.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |