---
UID : NE:strmini.STREAM_BUFFER_TYPE
title : STREAM_BUFFER_TYPE
author : windows-driver-content
description : This enumeration defines the buffer types for StreamClassGetPhysicalAddress.
old-location : stream\stream_buffer_type.htm
old-project : stream
ms.assetid : 7C9E1D94-BF59-4302-BEE8-24546C8AE7E6
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : STREAM_BUFFER_TYPE, STREAM_BUFFER_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : strmini.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : STREAM_BUFFER_TYPE
req.alt-loc : Strmini.h
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
req.typenames : STREAM_BUFFER_TYPE
req.product : Windows 10 or later.
---

# STREAM_BUFFER_TYPE Enumeration
This enumeration defines the buffer types for <a href="https://msdn.microsoft.com/library/windows/hardware/ff568247">StreamClassGetPhysicalAddress</a>.

## Syntax
````
typedef enum  { 
  PerRequestExtension,
  DmaBuffer,
  SRBDataBuffer
} STREAM_BUFFER_TYPE;
````

## Constants

<table>

<tr>
<td>DmaBuffer</td>
<td>Indicates the physical address of the DMA buffer.</td>
</tr>

<tr>
<td>PerRequestExtension</td>
<td>Indicates the physical address of the SRB extension.</td>
</tr>

<tr>
<td>SRBDataBuffer</td>
<td>Indicates the physical address of a data buffer.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | strmini.h |