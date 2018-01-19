---
UID : NE:ntddrilapitypes.RILUICCRESPONSEPARAMMASK
title : RILUICCRESPONSEPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\riluiccresponseparammask.htm
old-project : netvista
ms.assetid : 2a87655f-8c8c-48c7-982e-dcb70ca600fb
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILUICCRESPONSEPARAMMASK, RILUICCRESPONSEPARAMMASK
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
req.alt-api : RILUICCRESPONSEPARAMMASK
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
req.typenames : RILUICCRESPONSEPARAMMASK
---

# RILUICCRESPONSEPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILUICCRESPONSEPARAMMASK { 
  RIL_PARAM_SR_STATUSWORD2,
  RIL_PARAM_SR_RESPONSESIZE,
  RIL_PARAM_SR_RESPONSE,
  RIL_PARAM_SR_ALL
} RILUICCRESPONSEPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_SR_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SR_RESPONSE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SR_RESPONSESIZE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SR_STATUSWORD2</td>
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