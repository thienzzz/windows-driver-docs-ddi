---
UID : NE:rilapitypes.RILPERSODEACTIVATIONSTATEDEPERSOSTATE
title : RILPERSODEACTIVATIONSTATEDEPERSOSTATE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilpersodeactivationstatedepersostate_2.htm
old-project : netvista
ms.assetid : e01aa9fb-a35e-41d4-994b-8a166372caaf
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILPERSODEACTIVATIONSTATEDEPERSOSTATE, RILPERSODEACTIVATIONSTATEDEPERSOSTATE
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
req.alt-api : RILPERSODEACTIVATIONSTATEDEPERSOSTATE
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
req.typenames : RILPERSODEACTIVATIONSTATEDEPERSOSTATE
req.product : Windows 10 or later.
---

# RILPERSODEACTIVATIONSTATEDEPERSOSTATE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILPERSODEACTIVATIONSTATEDEPERSOSTATE { 
  RIL_DEPERSOSTATE_CK_REQUIRED,
  RIL_DEPERSOSTATE_PUK_REQUIRED,
  RIL_DEPERSOSTATE_PUK_BLOCKED,
  RIL_DEPERSOSTATE_MAX
} RILPERSODEACTIVATIONSTATEDEPERSOSTATE;
````

## Constants

<table>

<tr>
<td>RIL_DEPERSOSTATE_CK_REQUIRED</td>
<td></td>
</tr>

<tr>
<td>RIL_DEPERSOSTATE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_DEPERSOSTATE_PUK_BLOCKED</td>
<td></td>
</tr>

<tr>
<td>RIL_DEPERSOSTATE_PUK_REQUIRED</td>
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