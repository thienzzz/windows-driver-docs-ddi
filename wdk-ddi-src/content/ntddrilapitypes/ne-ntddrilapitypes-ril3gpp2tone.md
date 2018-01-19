---
UID : NE:ntddrilapitypes.RIL3GPP2TONE
title : RIL3GPP2TONE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\ril3gpp2tone.htm
old-project : netvista
ms.assetid : bf19de84-1c2d-4e9b-8061-888634dc2147
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RIL3GPP2TONE, RIL3GPP2TONE
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
req.alt-api : RIL3GPP2TONE
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
req.typenames : RIL3GPP2TONE
---

# RIL3GPP2TONE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RIL3GPP2TONE { 
  RIL_3GPP2TONE_DIAL,
  RIL_3GPP2TONE_RINGBACK,
  RIL_3GPP2TONE_INTERCEPT,
  RIL_3GPP2TONE_ABRVINTERCEPT,
  RIL_3GPP2TONE_REORDER,
  RIL_3GPP2TONE_ABRVREORDER,
  RIL_3GPP2TONE_BUSY,
  RIL_3GPP2TONE_CONFIRM,
  RIL_3GPP2TONE_ANSWER,
  RIL_3GPP2TONE_CALLWAITING,
  RIL_3GPP2TONE_PIP,
  RIL_3GPP2TONE_MAX
} RIL3GPP2TONE;
````

## Constants

<table>

<tr>
<td>RIL_3GPP2TONE_ABRVINTERCEPT</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_ABRVREORDER</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_ANSWER</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_BUSY</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_CALLWAITING</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_CONFIRM</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_DIAL</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_INTERCEPT</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_PIP</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_REORDER</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2TONE_RINGBACK</td>
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