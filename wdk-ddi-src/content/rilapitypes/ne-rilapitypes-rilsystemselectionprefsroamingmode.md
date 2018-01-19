---
UID : NE:rilapitypes.RILSYSTEMSELECTIONPREFSROAMINGMODE
title : RILSYSTEMSELECTIONPREFSROAMINGMODE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilsystemselectionprefsroamingmode_2.htm
old-project : netvista
ms.assetid : 7dbb25a5-7bcc-453d-854e-7796acbfd079
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILSYSTEMSELECTIONPREFSROAMINGMODE, RILSYSTEMSELECTIONPREFSROAMINGMODE
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
req.alt-api : RILSYSTEMSELECTIONPREFSROAMINGMODE
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
req.typenames : RILSYSTEMSELECTIONPREFSROAMINGMODE
req.product : Windows 10 or later.
---

# RILSYSTEMSELECTIONPREFSROAMINGMODE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILSYSTEMSELECTIONPREFSROAMINGMODE { 
  RIL_ROAMMODE_AUTOMATIC,
  RIL_ROAMMODE_DOMESTIC,
  RIL_ROAMMODE_MAX
} RILSYSTEMSELECTIONPREFSROAMINGMODE;
````

## Constants

<table>

<tr>
<td>RIL_ROAMMODE_AUTOMATIC</td>
<td></td>
</tr>

<tr>
<td>RIL_ROAMMODE_DOMESTIC</td>
<td></td>
</tr>

<tr>
<td>RIL_ROAMMODE_MAX</td>
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