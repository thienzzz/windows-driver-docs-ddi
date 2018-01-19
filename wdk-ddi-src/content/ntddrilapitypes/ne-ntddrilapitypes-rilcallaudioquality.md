---
UID : NE:ntddrilapitypes.RILCALLAUDIOQUALITY
title : RILCALLAUDIOQUALITY
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallaudioquality.htm
old-project : netvista
ms.assetid : bdd9879a-ec9b-431a-be95-4a1844e6238f
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLAUDIOQUALITY, RILCALLAUDIOQUALITY
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
req.alt-api : RILCALLAUDIOQUALITY
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
req.typenames : RILCALLAUDIOQUALITY
---

# RILCALLAUDIOQUALITY Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLAUDIOQUALITY { 
  RIL_CALLAUDIOQUALITY_STANDARD,
  RIL_CALLAUDIOQUALITY_HIGH,
  RIL_CALLAUDIOQUALITY_AMR_NB,
  RIL_CALLAUDIOQUALITY_AMR_WB,
  RIL_CALLAUDIOQUALITY_EVRC,
  RIL_CALLAUDIOQUALITY_EVRC_B,
  RIL_CALLAUDIOQUALITY_EVRC_NW,
  RIL_CALLAUDIOQUALITY_EVRC_WB,
  RIL_CALLAUDIOQUALITY_EVS_FB,
  RIL_CALLAUDIOQUALITY_EVS_NB,
  RIL_CALLAUDIOQUALITY_EVS_SWB,
  RIL_CALLAUDIOQUALITY_EVS_WB,
  RIL_CALLAUDIOQUALITY_GSM_EFR,
  RIL_CALLAUDIOQUALITY_GSM_FR,
  RIL_CALLAUDIOQUALITY_GSM_HR,
  RIL_CALLAUDIOQUALITY_QCELP13K,
  RIL_CALLAUDIOQUALITY_G711U,
  RIL_CALLAUDIOQUALITY_G711A,
  RIL_CALLAUDIOQUALITY_G722,
  RIL_CALLAUDIOQUALITY_G723,
  RIL_CALLAUDIOQUALITY_G729,
  RIL_CALLAUDIOQUALITY_MAX
} RILCALLAUDIOQUALITY;
````

## Constants

<table>

<tr>
<td>RIL_CALLAUDIOQUALITY_AMR_NB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_AMR_WB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVRC</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVRC_B</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVRC_NW</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVRC_WB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVS_FB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVS_NB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVS_SWB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_EVS_WB</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_G711A</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_G711U</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_G722</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_G723</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_G729</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_GSM_EFR</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_GSM_FR</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_GSM_HR</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_HIGH</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_QCELP13K</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLAUDIOQUALITY_STANDARD</td>
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