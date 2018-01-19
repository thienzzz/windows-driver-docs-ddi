---
UID : NE:ntddrilapitypes.RILGEOSCOPE
title : RILGEOSCOPE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilgeoscope.htm
old-project : netvista
ms.assetid : 5dc49d01-54d2-48d3-8649-96262b890fc5
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILGEOSCOPE, RILGEOSCOPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ntddrilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILGEOSCOPE
req.alt-loc : ntddrilapitypes.h
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
req.typenames : RILGEOSCOPE
---

# RILGEOSCOPE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILGEOSCOPE { 
  RIL_GEOSCOPE_CELL_IMMEDIATE,
  RIL_GEOSCOPE_LOCATIONAREA,
  RIL_GEOSCOPE_PLMN,
  RIL_GEOSCOPE_CELL,
  RIL_GEOSCOPE_MAX
} RILGEOSCOPE;
````

## Constants

<table>

<tr>
<td>RIL_GEOSCOPE_CELL</td>
<td></td>
</tr>

<tr>
<td>RIL_GEOSCOPE_CELL_IMMEDIATE</td>
<td></td>
</tr>

<tr>
<td>RIL_GEOSCOPE_LOCATIONAREA</td>
<td></td>
</tr>

<tr>
<td>RIL_GEOSCOPE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_GEOSCOPE_PLMN</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |