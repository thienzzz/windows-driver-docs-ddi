---
UID : NE:rilapitypes.RILOPERATORINFOPARAMMASK
title : RILOPERATORINFOPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\riloperatorinfoparammask_2.htm
old-project : netvista
ms.assetid : 1366f37b-4785-4e36-9fc8-bfaef6f9e227
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILOPERATORINFOPARAMMASK, RILOPERATORINFOPARAMMASK
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
req.alt-api : RILOPERATORINFOPARAMMASK
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
req.typenames : RILOPERATORINFOPARAMMASK
req.product : Windows 10 or later.
---

# RILOPERATORINFOPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILOPERATORINFOPARAMMASK { 
  RIL_PARAM_OI_STATUS,
  RIL_PARAM_OI_NAMES,
  RIL_PARAM_OI_ALL
} RILOPERATORINFOPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_OI_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_OI_NAMES</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_OI_STATUS</td>
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