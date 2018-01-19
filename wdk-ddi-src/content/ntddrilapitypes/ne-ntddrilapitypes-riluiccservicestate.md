---
UID : NE:ntddrilapitypes.RILUICCSERVICESTATE
title : RILUICCSERVICESTATE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\riluiccservicestate.htm
old-project : netvista
ms.assetid : 01d64333-3f49-45e1-bd2b-dda0aeb6a083
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILUICCSERVICESTATE, RILUICCSERVICESTATE
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
req.alt-api : RILUICCSERVICESTATE
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
req.typenames : RILUICCSERVICESTATE
---

# RILUICCSERVICESTATE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILUICCSERVICESTATE { 
  RIL_UICCSERVICESTATE_DISABLED,
  RIL_UICCSERVICESTATE_ENABLED,
  RIL_UICCSERVICESTATE_MAX
} RILUICCSERVICESTATE;
````

## Constants

<table>

<tr>
<td>RIL_UICCSERVICESTATE_DISABLED</td>
<td></td>
</tr>

<tr>
<td>RIL_UICCSERVICESTATE_ENABLED</td>
<td></td>
</tr>

<tr>
<td>RIL_UICCSERVICESTATE_MAX</td>
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