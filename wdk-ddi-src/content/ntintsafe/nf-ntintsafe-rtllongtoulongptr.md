---
UID : NF:ntintsafe.RtlLongToULongPtr
title : RtlLongToULongPtr function
author : windows-driver-content
description : Converts a value of type LONG to a value of type ULONG_PTR.
old-location : kernel\rtllongtoulongptr.htm
old-project : kernel
ms.assetid : D05EDC76-7A3E-4A9F-8950-8E54CDD16016
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlLongToULongPtr
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
req.alt-api : RtlLongToULongPtr
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


# RtlLongToULongPtr function
Converts a value of type <b>LONG</b> to a value of type <b>ULONG_PTR</b>.

## Syntax

````
NTSTATUS RtlLongToULongPtr(
  _In_  LONG      ulOperand,
  _Out_ ULONG_PTR *pusResult
);
````

## Parameters

`lOperand`



`pulResult`




## Return Value

None

## Remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

This function uses the following alternate name:</p>

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