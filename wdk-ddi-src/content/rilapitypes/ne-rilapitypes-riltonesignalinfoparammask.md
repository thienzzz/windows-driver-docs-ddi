---
UID : NE:rilapitypes.RILTONESIGNALINFOPARAMMASK
title : RILTONESIGNALINFOPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\riltonesignalinfoparammask_2.htm
old-project : netvista
ms.assetid : 1eeca3ef-6e1d-486f-b700-5ab8718a9285
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILTONESIGNALINFOPARAMMASK, RILTONESIGNALINFOPARAMMASK
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
req.alt-api : RILTONESIGNALINFOPARAMMASK
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
req.typenames : RILTONESIGNALINFOPARAMMASK
req.product : Windows 10 or later.
---

# RILTONESIGNALINFOPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILTONESIGNALINFOPARAMMASK { 
  RIL_PARAM_TONESIGNAL_GPP2TONE,
  RIL_PARAM_TONESIGNAL_GPP2ISDNALERTING,
  RIL_PARAM_TONESIGNAL_EXECUTOR,
  RIL_PARAM_TONESIGNAL_All
} RILTONESIGNALINFOPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_TONESIGNAL_All</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_TONESIGNAL_EXECUTOR</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_TONESIGNAL_GPP2ISDNALERTING</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_TONESIGNAL_GPP2TONE</td>
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