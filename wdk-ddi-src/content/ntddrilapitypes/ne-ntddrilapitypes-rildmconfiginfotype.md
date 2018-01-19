---
UID : NE:ntddrilapitypes.RILDMCONFIGINFOTYPE
title : RILDMCONFIGINFOTYPE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rildmconfiginfotype.htm
old-project : netvista
ms.assetid : c6dc14a5-59de-42dd-9e45-99f632bf6a57
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILDMCONFIGINFOTYPE, RILDMCONFIGINFOTYPE
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
req.alt-api : RILDMCONFIGINFOTYPE
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
req.typenames : RILDMCONFIGINFOTYPE
---

# RILDMCONFIGINFOTYPE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILDMCONFIGINFOTYPE { 
  RIL_DMCV_TYPE_BOOLEAN,
  RIL_DMCV_TYPE_DWORD,
  RIL_DMCV_TYPE_STRING,
  RIL_DMCV_TYPE_MAX
} RILDMCONFIGINFOTYPE;
````

## Constants

<table>

<tr>
<td>RIL_DMCV_TYPE_BOOLEAN</td>
<td></td>
</tr>

<tr>
<td>RIL_DMCV_TYPE_DWORD</td>
<td></td>
</tr>

<tr>
<td>RIL_DMCV_TYPE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_DMCV_TYPE_STRING</td>
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