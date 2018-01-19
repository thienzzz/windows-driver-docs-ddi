---
UID : NF:ndis.NdisGetSharedDataAlignment
title : NdisGetSharedDataAlignment function
author : windows-driver-content
description : NdisGetSharedDataAlignment returns the preferred alignment for memory structures that can be shared by more than one processor.
old-location : netvista\ndisgetshareddataalignment.htm
old-project : netvista
ms.assetid : 561315b4-8866-4f48-8138-12b1a38f743e
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisGetSharedDataAlignment
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Universal
req.target-min-winverclnt : Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisGetSharedDataAlignment   (NDIS 5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see    NdisGetSharedDataAlignment   (NDIS 5.1)) in Windows XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisGetSharedDataAlignment
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : Irql_Miscellaneous_Function
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ndis.lib
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisGetSharedDataAlignment function
<b>NdisGetSharedDataAlignment</b> returns the preferred alignment for memory structures that can be shared
  by more than one processor.

## Syntax

````
ULONG NdisGetSharedDataAlignment(void);
````

## Parameters

This function has no parameters.

## Return Value

The boundary value, in bytes, on which drivers should align structures that can be shared by more
     than one processor.

The boundary value, in bytes, on which drivers should align structures that can be shared by more
     than one processor.

The boundary value, in bytes, on which drivers should align structures that can be shared by more
     than one processor.

## Remarks

Use 
    <b>NdisGetSharedDataAlignment</b> to determine the best alignment for data structures that will be shared
    between processors. Using the returned value when allocating such structures minimizes cache effects that
    reduce the performance of multiprocessor systems.

System support for 
    <b>NdisGetSharedDataAlignment</b> is available in Windows XP and later versions.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** | Irql_Miscellaneous_Function |