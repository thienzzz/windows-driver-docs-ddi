---
UID : NE:rilapitypes.RILMSGCDMAMSGSTATUSTYPE
title : RILMSGCDMAMSGSTATUSTYPE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmsgcdmamsgstatustype_2.htm
old-project : netvista
ms.assetid : 315ca5af-103e-4c00-8dd7-10aa21bfa8a2
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMSGCDMAMSGSTATUSTYPE, RILMSGCDMAMSGSTATUSTYPE
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
req.alt-api : RILMSGCDMAMSGSTATUSTYPE
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
req.typenames : RILMSGCDMAMSGSTATUSTYPE
req.product : Windows 10 or later.
---

# RILMSGCDMAMSGSTATUSTYPE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILMSGCDMAMSGSTATUSTYPE { 
  RIL_MSGSTATUSTYPE_DELIVERYACK,
  RIL_MSGSTATUSTYPE_USERACK,
  RIL_MSGSTATUSTYPE_READACK,
  RIL_MSGSTATUSTYPE_MAX
} RILMSGCDMAMSGSTATUSTYPE;
````

## Constants

<table>

<tr>
<td>RIL_MSGSTATUSTYPE_DELIVERYACK</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGSTATUSTYPE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGSTATUSTYPE_READACK</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGSTATUSTYPE_USERACK</td>
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