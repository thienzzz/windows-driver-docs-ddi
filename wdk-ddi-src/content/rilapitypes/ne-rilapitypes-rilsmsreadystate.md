---
UID : NE:rilapitypes.RILSMSREADYSTATE
title : RILSMSREADYSTATE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilsmsreadystate_2.htm
old-project : netvista
ms.assetid : 4b1fd540-85cf-45b3-9f39-984bb3b9e200
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILSMSREADYSTATE, RILSMSREADYSTATE
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
req.alt-api : RILSMSREADYSTATE
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
req.typenames : RILSMSREADYSTATE
req.product : Windows 10 or later.
---

# RILSMSREADYSTATE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILSMSREADYSTATE { 
  RIL_SMSREADY_SERVICEREADY_3GPP2,
  RIL_SMSREADY_UICCREADY,
  RIL_SMSREADYSTATE_ALL
} RILSMSREADYSTATE;
````

## Constants

<table>

<tr>
<td>RIL_SMSREADY_SERVICEREADY_3GPP2</td>
<td></td>
</tr>

<tr>
<td>RIL_SMSREADY_UICCREADY</td>
<td></td>
</tr>

<tr>
<td>RIL_SMSREADYSTATE_ALL</td>
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