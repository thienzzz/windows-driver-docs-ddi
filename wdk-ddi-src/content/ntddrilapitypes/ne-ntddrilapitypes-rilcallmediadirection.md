---
UID : NE:ntddrilapitypes.RILCALLMEDIADIRECTION
title : RILCALLMEDIADIRECTION
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallmediadirection.htm
old-project : netvista
ms.assetid : 8c6b2329-9956-43c1-8a4d-ef9587cf0980
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLMEDIADIRECTION, RILCALLMEDIADIRECTION
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
req.alt-api : RILCALLMEDIADIRECTION
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
req.typenames : RILCALLMEDIADIRECTION
---

# RILCALLMEDIADIRECTION Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLMEDIADIRECTION { 
  RIL_CALLMEDIADIRECTION_RX,
  RIL_CALLMEDIADIRECTION_TX,
  RIL_CALLMEDIADIRECTION_RXTX,
  RIL_CALLMEDIADIRECTION_MAX
} RILCALLMEDIADIRECTION;
````

## Constants

<table>

<tr>
<td>RIL_CALLMEDIADIRECTION_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLMEDIADIRECTION_RX</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLMEDIADIRECTION_RXTX</td>
<td></td>
</tr>

<tr>
<td>RIL_CALLMEDIADIRECTION_TX</td>
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