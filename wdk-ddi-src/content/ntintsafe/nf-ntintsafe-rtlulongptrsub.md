---
UID : NF:ntintsafe.RtlULongPtrSub
title : RtlULongPtrSub function
author : windows-driver-content
description : Subtracts one value of type ULONG_PTR from another.
old-location : kernel\rtlulongptrsub.htm
old-project : kernel
ms.assetid : E8F9A1B0-5E87-4CB0-8C9E-5C2494F07C39
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlULongPtrSub
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
req.alt-api : RtlULongPtrSub
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


# RtlULongPtrSub function
Subtracts one value of type <b>ULONG_PTR</b> from another.

## Syntax

````
NTSTATUS RtlULongPtrSub(
  _In_  ULONG_PTR ulMinuend,
  _In_  ULONG_PTR ulSubtrahend,
  _Out_ ULONG_PTR *pulResult
);
````

## Parameters

`ulMinuend`

The value from which <i>ulSubtrahend</i> is subtracted.

`ulSubtrahend`

The value to subtract from <i>ulMinuend</i>.

`pulResult`

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