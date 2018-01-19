---
UID : NE:ntddrilapitypes.RILCALLAUDIOSOURCE
title : RILCALLAUDIOSOURCE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallaudiosource.htm
old-project : netvista
ms.assetid : ec6d45ba-3afe-44cb-a699-ef3b3b804b6b
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLAUDIOSOURCE, RILCALLAUDIOSOURCE
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
req.alt-api : RILCALLAUDIOSOURCE
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
req.typenames : RILCALLAUDIOSOURCE
---

# RILCALLAUDIOSOURCE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLAUDIOSOURCE { 
  RIL_CALLAUDIOSOURCE_PKT_MODEM,
  RIL_CALLAUDIOSOURCE_PKT_APP,
  RIL_CALLAUDIOSOURCE_MAX
} RILCALLAUDIOSOURCE;
````

## Constants

<table>

<tr>
<td>RIL_CALLAUDIOSOURCE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOSOURCE_PKT_APP</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOSOURCE_PKT_MODEM</td>
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