---
UID : NE:ksproxy.PIPE_ALLOCATOR_PLACE
title : PIPE_ALLOCATOR_PLACE
author : windows-driver-content
description : .
old-location : stream\pipe_allocator_place.htm
old-project : stream
ms.assetid : 86B1D8BB-7213-403C-8EAB-D681A5DBF49E
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : PIPE_ALLOCATOR_PLACE, PIPE_ALLOCATOR_PLACE, *PPIPE_ALLOCATOR_PLACE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ksproxy.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PIPE_ALLOCATOR_PLACE
req.alt-loc : Ksproxy.h
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
req.typenames : PIPE_ALLOCATOR_PLACE
---

# PIPE_ALLOCATOR_PLACE Enumeration


## Syntax
````
typedef enum  { 
  Pipe_Allocator_None,
  Pipe_Allocator_FirstPin,
  Pipe_Allocator_LastPin,
  Pipe_Allocator_MiddlePin
} PIPE_ALLOCATOR_PLACE;
````

## Constants

<table>

<tr>
<td>Pipe_Allocator_FirstPin</td>
<td></td>
</tr>

<tr>
<td>Pipe_Allocator_LastPin</td>
<td></td>
</tr>

<tr>
<td>Pipe_Allocator_MiddlePin</td>
<td></td>
</tr>

<tr>
<td>Pipe_Allocator_None</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ksproxy.h |