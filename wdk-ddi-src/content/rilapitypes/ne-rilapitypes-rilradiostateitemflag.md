---
UID : NE:rilapitypes.RILRADIOSTATEITEMFLAG
title : RILRADIOSTATEITEMFLAG
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilradiostateitemflag_2.htm
old-project : netvista
ms.assetid : 1cf1ebcb-423e-42ee-97aa-bd5f6516e65b
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILRADIOSTATEITEMFLAG, RILRADIOSTATEITEMFLAG
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : rilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILRADIOSTATEITEMFLAG
req.alt-loc : rilapitypes.h
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
req.typenames : RILRADIOSTATEITEMFLAG
req.product : Windows 10 or later.
---

# RILRADIOSTATEITEMFLAG Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILRADIOSTATEITEMFLAG { 
  RIL_RADIOSTATE_ITEMFLAG_USE_UINTVAL,
  RIL_RADIOSTATE_ITEMFLAG_USE_WSZVAL,
  RIL_RADIOSTATE_ITEMFLAG_USE_INTARRAY,
  RIL_RADIOSTATE_ITEMFLAG_USE_UINTARRAY,
  RIL_RADIOSTATE_ITEMFLAG_USE_BYTEARRAY,
  RIL_RADIOSTATE_ITEMFLAG_USE_MAX
} RILRADIOSTATEITEMFLAG;
````

## Constants

<table>

<tr>
<td>RIL_RADIOSTATE_ITEMFLAG_USE_BYTEARRAY</td>
<td></td>
</tr>

<tr>
<td>RIL_RADIOSTATE_ITEMFLAG_USE_INTARRAY</td>
<td></td>
</tr>

<tr>
<td>RIL_RADIOSTATE_ITEMFLAG_USE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_RADIOSTATE_ITEMFLAG_USE_UINTARRAY</td>
<td></td>
</tr>

<tr>
<td>RIL_RADIOSTATE_ITEMFLAG_USE_UINTVAL</td>
<td></td>
</tr>

<tr>
<td>RIL_RADIOSTATE_ITEMFLAG_USE_WSZVAL</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapitypes.h |