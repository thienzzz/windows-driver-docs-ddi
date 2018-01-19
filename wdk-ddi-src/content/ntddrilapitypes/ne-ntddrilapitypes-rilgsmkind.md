---
UID : NE:ntddrilapitypes.RILGSMKIND
title : RILGSMKIND
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilgsmkind.htm
old-project : netvista
ms.assetid : ad88382b-bfb0-46c4-9db7-9adb1ee074a4
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILGSMKIND, RILGSMKIND
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
req.alt-api : RILGSMKIND
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
req.typenames : RILGSMKIND
---

# RILGSMKIND Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILGSMKIND { 
  RIL_GSMKIND_GPRS,
  RIL_GSMKIND_EDGE,
  RIL_GSMKIND_MAX
} RILGSMKIND;
````

## Constants

<table>

<tr>
<td>RIL_GSMKIND_EDGE</td>
<td></td>
</tr>

<tr>
<td>RIL_GSMKIND_GPRS</td>
<td></td>
</tr>

<tr>
<td>RIL_GSMKIND_MAX</td>
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