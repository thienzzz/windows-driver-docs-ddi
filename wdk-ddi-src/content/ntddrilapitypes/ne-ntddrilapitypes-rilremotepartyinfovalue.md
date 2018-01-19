---
UID : NE:ntddrilapitypes.RILREMOTEPARTYINFOVALUE
title : RILREMOTEPARTYINFOVALUE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilremotepartyinfovalue.htm
old-project : netvista
ms.assetid : 9cc766c4-a2c0-4b84-a4d8-b005cddd9eea
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILREMOTEPARTYINFOVALUE, RILREMOTEPARTYINFOVALUE
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
req.alt-api : RILREMOTEPARTYINFOVALUE
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
req.typenames : RILREMOTEPARTYINFOVALUE
---

# RILREMOTEPARTYINFOVALUE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILREMOTEPARTYINFOVALUE { 
  RIL_REMOTEPARTYINFO_WITHHELD,
  RIL_REMOTEPARTYINFO_UNAVAILABLE,
  RIL_REMOTEPARTYINFO_MAX
} RILREMOTEPARTYINFOVALUE;
````

## Constants

<table>

<tr>
<td>RIL_REMOTEPARTYINFO_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_REMOTEPARTYINFO_UNAVAILABLE</td>
<td></td>
</tr>

<tr>
<td>RIL_REMOTEPARTYINFO_WITHHELD</td>
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