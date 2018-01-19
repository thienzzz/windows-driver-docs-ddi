---
UID : NE:rilapitypes.RILCALLINFODISCONNECTREASON
title : RILCALLINFODISCONNECTREASON
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallinfodisconnectreason_2.htm
old-project : netvista
ms.assetid : b0cc8ecb-fa13-414a-b08a-de0d60724f25
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLINFODISCONNECTREASON, RILCALLINFODISCONNECTREASON
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
req.alt-api : RILCALLINFODISCONNECTREASON
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
req.typenames : RILCALLINFODISCONNECTREASON
req.product : Windows 10 or later.
---

# RILCALLINFODISCONNECTREASON Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLINFODISCONNECTREASON { 
  RIL_DISCREASON_BUSY,
  RIL_DISCREASON_NETWORKERROR,
  RIL_DISCREASON_RADIOFADE,
  RIL_DISCREASON_CONGESTION,
  RIL_DISCREASON_EMERGENCYONLY,
  RIL_DISCREASON_NOSERVICE,
  RIL_DISCREASON_OTHEREXECUTORBUSY,
  RIL_DISCREASON_EMERGENCYFAILOVER,
  RIL_DISCREASON_HANDOVER_MERGE,
  RIL_DISCREASON_MAX
} RILCALLINFODISCONNECTREASON;
````

## Constants

<table>

<tr>
<td>RIL_DISCREASON_BUSY</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_CONGESTION</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_EMERGENCYFAILOVER</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_EMERGENCYONLY</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_HANDOVER_MERGE</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_NETWORKERROR</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_NOSERVICE</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_OTHEREXECUTORBUSY</td>
<td></td>
</tr>

<tr>
<td>RIL_DISCREASON_RADIOFADE</td>
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