---
UID : NE:ntddrilapitypes.RIL3GPP2ISDNALERTING
title : RIL3GPP2ISDNALERTING
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\ril3gpp2isdnalerting.htm
old-project : netvista
ms.assetid : e3ba9bdd-2741-4a6c-9613-1ced31fc3dbf
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RIL3GPP2ISDNALERTING, RIL3GPP2ISDNALERTING
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
req.alt-api : RIL3GPP2ISDNALERTING
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
req.typenames : RIL3GPP2ISDNALERTING
---

# RIL3GPP2ISDNALERTING Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RIL3GPP2ISDNALERTING { 
  RIL_3GPP2ISDNALERTING_NORMAL,
  RIL_3GPP2ISDNALERTING_INTERGROUP,
  RIL_3GPP2ISDNALERTING_SPECIAL,
  RIL_3GPP2ISDNALERTING_PINGRING,
  RIL_3GPP2ISDNALERTING_MAX
} RIL3GPP2ISDNALERTING;
````

## Constants

<table>

<tr>
<td>RIL_3GPP2ISDNALERTING_INTERGROUP</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2ISDNALERTING_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2ISDNALERTING_NORMAL</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2ISDNALERTING_PINGRING</td>
<td></td>
</tr>

<tr>
<td>RIL_3GPP2ISDNALERTING_SPECIAL</td>
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