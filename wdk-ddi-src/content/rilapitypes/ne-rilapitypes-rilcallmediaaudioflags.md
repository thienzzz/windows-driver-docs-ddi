---
UID : NE:rilapitypes.RILCALLMEDIAAUDIOFLAGS
title : RILCALLMEDIAAUDIOFLAGS
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallmediaaudioflags_2.htm
old-project : netvista
ms.assetid : da09298f-88be-44ef-8072-d11cf91401c7
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLMEDIAAUDIOFLAGS, RILCALLMEDIAAUDIOFLAGS
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
req.alt-api : RILCALLMEDIAAUDIOFLAGS
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
req.typenames : RILCALLMEDIAAUDIOFLAGS
req.product : Windows 10 or later.
---

# RILCALLMEDIAAUDIOFLAGS Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLMEDIAAUDIOFLAGS { 
  RIL_CALLMEDIAAUDIOFLAG_TEMPORARILY_UNAVAILABLE,
  RIL_CALLMEDIAAUDIOFLAG_ALL
} RILCALLMEDIAAUDIOFLAGS;
````

## Constants

<table>

<tr>
<td>RIL_CALLMEDIAAUDIOFLAG_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLMEDIAAUDIOFLAG_TEMPORARILY_UNAVAILABLE</td>
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