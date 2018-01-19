---
UID : NE:ntddrilapitypes.RILRFSTATEPARAMMASK
title : RILRFSTATEPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilrfstateparammask.htm
old-project : netvista
ms.assetid : 53cd2444-fda7-4e1f-b2d3-23ab20955a0e
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILRFSTATEPARAMMASK, RILRFSTATEPARAMMASK
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
req.alt-api : RILRFSTATEPARAMMASK
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
req.typenames : RILRFSTATEPARAMMASK
---

# RILRFSTATEPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILRFSTATEPARAMMASK { 
  RIL_PARAM_RFSTATE_RFSTATE,
  RIL_PARAM_RFSTATE_RFDATASIZE,
  RIL_PARAM_RFSTATE_RFDATA,
  RIL_PARAM_RFSTATE_ALL
} RILRFSTATEPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_RFSTATE_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_RFSTATE_RFDATA</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_RFSTATE_RFDATASIZE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_RFSTATE_RFSTATE</td>
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