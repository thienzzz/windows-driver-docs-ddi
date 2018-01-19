---
UID : NE:ntddrilapitypes.RILMESSAGETYPE
title : RILMESSAGETYPE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmessagetype.htm
old-project : netvista
ms.assetid : 02960e7c-f1b2-4c28-9f9b-f180df3d9563
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMESSAGETYPE, RILMESSAGETYPE
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
req.alt-api : RILMESSAGETYPE
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
req.typenames : RILMESSAGETYPE
---

# RILMESSAGETYPE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILMESSAGETYPE { 
  RIL_MSGTYPE_IN_STATUS,
  RIL_MSGTYPE_IN_IS637STATUS,
  RIL_MSGTYPE_IN_CDMADELIVER,
  RIL_MSGTYPE_OUT_SUBMIT,
  RIL_MSGTYPE_OUT_CDMASUBMIT,
  RIL_MSGTYPE_BC_GENERAL
} RILMESSAGETYPE;
````

## Constants

<table>

<tr>
<td>RIL_MSGTYPE_BC_GENERAL</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTYPE_IN_CDMADELIVER</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTYPE_IN_IS637STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTYPE_IN_STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTYPE_OUT_CDMASUBMIT</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTYPE_OUT_SUBMIT</td>
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