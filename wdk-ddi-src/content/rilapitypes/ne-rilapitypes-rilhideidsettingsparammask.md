---
UID : NE:rilapitypes.RILHIDEIDSETTINGSPARAMMASK
title : RILHIDEIDSETTINGSPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilhideidsettingsparammask_2.htm
old-project : netvista
ms.assetid : 5c951b21-1fa9-4b76-8631-3ab4148176ef
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILHIDEIDSETTINGSPARAMMASK, RILHIDEIDSETTINGSPARAMMASK
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
req.alt-api : RILHIDEIDSETTINGSPARAMMASK
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
req.typenames : RILHIDEIDSETTINGSPARAMMASK
req.product : Windows 10 or later.
---

# RILHIDEIDSETTINGSPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILHIDEIDSETTINGSPARAMMASK { 
  RIL_PARAM_HIDS_STATUS,
  RIL_PARAM_HIDS_PROVISIONING,
  RIL_PARAM_HIDS_ALL
} RILHIDEIDSETTINGSPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_HIDS_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_HIDS_PROVISIONING</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_HIDS_STATUS</td>
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