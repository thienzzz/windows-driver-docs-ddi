---
UID : NF:ntintsafe.RtlIntSub
title : RtlIntSub function
author : windows-driver-content
description : Subtracts one value of type INT from another.
old-location : kernel\rtlintsub.htm
old-project : kernel
ms.assetid : 68BBD6B8-5C7C-4FE5-97F7-473A9510400F
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlIntSub
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
req.alt-api : RtlIntSub
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


# RtlIntSub function
Subtracts one value of type <b>INT</b> from another.

## Syntax

````
NTSTATUS RtlIntSub(
  _In_  INT iMinuend,
  _In_  INT iSubtrahend,
  _Out_ INT *pu8Result
);
````

## Parameters

`iMinuend`

The value from which <i>iSubtrahend</i> is subtracted.

`iSubtrahend`

The value to subtract from <i>iMinuend</i>.

`piResult`




## Return Value

None

## Remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

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