---
UID : NE:ks.KSMETHOD_STREAMALLOCATOR
title : KSMETHOD_STREAMALLOCATOR
author : windows-driver-content
description : .
old-location : stream\ksmethod_streamallocator.htm
old-project : stream
ms.assetid : 2CADC0BF-D8C0-48EC-8206-E1BD61DF4AD7
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : KSMETHOD_STREAMALLOCATOR, KSMETHOD_STREAMALLOCATOR
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ks.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KSMETHOD_STREAMALLOCATOR
req.alt-loc : Ks.h
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
req.typenames : KSMETHOD_STREAMALLOCATOR
---

# KSMETHOD_STREAMALLOCATOR Enumeration


## Syntax
````
typedef enum  { 
  KSMETHOD_STREAMALLOCATOR_ALLOC,
  KSMETHOD_STREAMALLOCATOR_FREE
} KSMETHOD_STREAMALLOCATOR;
````

## Constants

<table>

<tr>
<td>KSMETHOD_STREAMALLOCATOR_ALLOC</td>
<td></td>
</tr>

<tr>
<td>KSMETHOD_STREAMALLOCATOR_FREE</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ks.h |