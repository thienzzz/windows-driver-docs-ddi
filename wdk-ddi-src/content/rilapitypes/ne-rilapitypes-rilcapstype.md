---
UID : NE:rilapitypes.RILCAPSTYPE
title : RILCAPSTYPE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcapstype_2.htm
old-project : netvista
ms.assetid : 492436da-9d6f-462b-9c4d-4466cb2f78f6
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCAPSTYPE, RILCAPSTYPE
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
req.alt-api : RILCAPSTYPE
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
req.typenames : RILCAPSTYPE
req.product : Windows 10 or later.
---

# RILCAPSTYPE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCAPSTYPE { 
  RIL_CAPSTYPE_PERSOLOCKPWDLENGTH,
  RIL_CAPSTYPE_PBMAXREAD,
  RIL_CAPSTYPE_PBSTORELOCATIONS,
  RIL_CAPSTYPE_RADIOCONFIGURATIONS,
  RIL_CAPSTYPE_SIGNALQUALITYIMPLEMENTATION,
  RIL_CAPSTYPE_NITZNOTIFICATION,
  RIL_CAPSTYPE_CALLSUPPORT,
  RIL_CAPSTYPE_SMSSUPPORT,
  RIL_CAPSTYPE_ARG_SMALLEST,
  RIL_CAPSTYPE_ARG_LARGEST,
  RIL_CAPSTYPE_MAX
} RILCAPSTYPE;
````

## Constants

<table>

<tr>
<td>RIL_CAPSTYPE_ARG_LARGEST</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_ARG_SMALLEST</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_CALLSUPPORT</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_NITZNOTIFICATION</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_PBMAXREAD</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_PBSTORELOCATIONS</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_PERSOLOCKPWDLENGTH</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_RADIOCONFIGURATIONS</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_SIGNALQUALITYIMPLEMENTATION</td>
<td></td>
</tr>

<tr>
<td>RIL_CAPSTYPE_SMSSUPPORT</td>
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