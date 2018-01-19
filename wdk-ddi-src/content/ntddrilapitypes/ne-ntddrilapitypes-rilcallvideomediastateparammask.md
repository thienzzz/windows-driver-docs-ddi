---
UID : NE:ntddrilapitypes.RILCALLVIDEOMEDIASTATEPARAMMASK
title : RILCALLVIDEOMEDIASTATEPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallvideomediastateparammask.htm
old-project : netvista
ms.assetid : e36617c0-8471-417d-9135-bdd29c586172
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLVIDEOMEDIASTATEPARAMMASK, RILCALLVIDEOMEDIASTATEPARAMMASK
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
req.alt-api : RILCALLVIDEOMEDIASTATEPARAMMASK
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
req.typenames : RILCALLVIDEOMEDIASTATEPARAMMASK
---

# RILCALLVIDEOMEDIASTATEPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLVIDEOMEDIASTATEPARAMMASK { 
  RIL_PARAM_CALLVIDEO_FLAGS,
  RIL_PARAM_CALLVIDEO_CONTEXTID,
  RIL_PARAM_CALLVIDEO_ALL
} RILCALLVIDEOMEDIASTATEPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_CALLVIDEO_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CALLVIDEO_CONTEXTID</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CALLVIDEO_FLAGS</td>
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