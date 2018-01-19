---
UID : NE:rilapitypes.RILCALLINFODISCONNECTINITIATOR
title : RILCALLINFODISCONNECTINITIATOR
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallinfodisconnectinitiator_2.htm
old-project : netvista
ms.assetid : 4ea730ab-0ba0-46cd-b156-0b2f32b2eafe
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLINFODISCONNECTINITIATOR, RILCALLINFODISCONNECTINITIATOR
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
req.alt-api : RILCALLINFODISCONNECTINITIATOR
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
req.typenames : RILCALLINFODISCONNECTINITIATOR
req.product : Windows 10 or later.
---

# RILCALLINFODISCONNECTINITIATOR Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLINFODISCONNECTINITIATOR { 
  RIL_DISCINIT_LOCAL,
  RIL_DISCINIT_REMOTE,
  RIL_DISCINIT_MAX
} RILCALLINFODISCONNECTINITIATOR;
````

## Constants

<table>

<tr>
<td>RIL_DISCINIT_LOCAL</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCINIT_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCINIT_REMOTE</td>
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