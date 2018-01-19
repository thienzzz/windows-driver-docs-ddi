---
UID : NE:ntddrilapitypes.RILPERSOLOCKSUPPORTCAPS
title : RILPERSOLOCKSUPPORTCAPS
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilpersolocksupportcaps.htm
old-project : netvista
ms.assetid : 1aeb5eef-c334-4e27-8ce9-1c8efc85e82c
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILPERSOLOCKSUPPORTCAPS, RILPERSOLOCKSUPPORTCAPS
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
req.alt-api : RILPERSOLOCKSUPPORTCAPS
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
req.typenames : RILPERSOLOCKSUPPORTCAPS
---

# RILPERSOLOCKSUPPORTCAPS Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILPERSOLOCKSUPPORTCAPS { 
  RIL_CAPS_PERSOFEATURE_3GPP_NETSUB,
  RIL_CAPS_PERSOFEATURE_3GPP_SP,
  RIL_CAPS_PERSOFEATURE_3GPP_CORP,
  RIL_CAPS_PERSOFEATURE_3GPP_USIM,
  RIL_CAPS_PERSOFEATURE_3GPP2_NETTYPE1,
  RIL_CAPS_PERSOFEATURE_3GPP2_NETTYPE2,
  RIL_CAPS_PERSOFEATURE_3GPP2_HRPD,
  RIL_CAPS_PERSOFEATURE_3GPP2_SP,
  RIL_CAPS_PERSOFEATURE_3GPP2_CORP,
  RIL_CAPS_PERSOFEATURE_3GPP2_UIM,
  RIL_CAPS_PERSOFEATURE_ALL
} RILPERSOLOCKSUPPORTCAPS;
````

## Constants

<table>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP_CORP</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP_NETSUB</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP_SP</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP_USIM</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP2_CORP</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP2_HRPD</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP2_NETTYPE1</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP2_NETTYPE2</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP2_SP</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_3GPP2_UIM</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPS_PERSOFEATURE_ALL</td>
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