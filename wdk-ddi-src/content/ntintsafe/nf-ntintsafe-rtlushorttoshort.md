---
UID : NF:ntintsafe.RtlUShortToShort
title : RtlUShortToShort function
author : windows-driver-content
description : Converts a value of type USHORT to a value of type SHORT.
old-location : kernel\rtlushorttoshort.htm
old-project : kernel
ms.assetid : 055B5605-2EBB-4B09-9C21-A8288D0DB3CD
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlUShortToShort
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
req.alt-api : RtlUShortToShort
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


# RtlUShortToShort function
Converts a value of type <b>USHORT</b> to a value of type <b>SHORT</b>.

## Syntax

````
NTSTATUS RtlUShortToShort(
  _In_  USHORT usOperand,
  _Out_ SHORT  *psResult
);
````

## Parameters

`usOperand`

The value to be converted.

`psResult`

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## Return Value

None

## Remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.</p>

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