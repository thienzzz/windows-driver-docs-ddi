---
UID : NF:ntintsafe.RtlULongLongAdd
title : RtlULongLongAdd function
author : windows-driver-content
description : Adds two values of type ULONGLONG.
old-location : kernel\rtlulonglongadd.htm
old-project : kernel
ms.assetid : AE58D20E-25A0-4D45-9E60-38EF2F1D1EF3
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlULongLongAdd
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
req.alt-api : RtlULongLongAdd
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


# RtlULongLongAdd function
Adds two values of type <b>ULONGLONG</b>.

## Syntax

````
NTSTATUS RtlULongLongAdd(
  _In_  ULONGLONG ullAugend,
  _In_  ULONGLONG ullAddend,
  _Out_ ULONGLONG *pllResult
);
````

## Parameters

`ullAugend`

The first value in the equation.

`ullAddend`

The value to add to <i>ullAugend</i>.

`pullResult`




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