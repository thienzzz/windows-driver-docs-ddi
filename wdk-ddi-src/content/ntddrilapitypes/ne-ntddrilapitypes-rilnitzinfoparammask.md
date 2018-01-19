---
UID : NE:ntddrilapitypes.RILNITZINFOPARAMMASK
title : RILNITZINFOPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilnitzinfoparammask.htm
old-project : netvista
ms.assetid : bdf1505f-2a84-48a3-9534-df83237ab7bb
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILNITZINFOPARAMMASK, RILNITZINFOPARAMMASK
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
req.alt-api : RILNITZINFOPARAMMASK
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
req.typenames : RILNITZINFOPARAMMASK
---

# RILNITZINFOPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILNITZINFOPARAMMASK { 
  RIL_PARAM_NITZ_TIMEZONEOFFSET,
  RIL_PARAM_NITZ_DAYLIGHTSAVINGOFFSET,
  RIL_PARAM_NITZ_SYSTEMTIME,
  RIL_PARAM_NITZ_SYSTEMTYPE,
  RIL_PARAM_NITZ_ALL
} RILNITZINFOPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_NITZ_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_NITZ_DAYLIGHTSAVINGOFFSET</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_NITZ_SYSTEMTIME</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_NITZ_SYSTEMTYPE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_NITZ_TIMEZONEOFFSET</td>
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