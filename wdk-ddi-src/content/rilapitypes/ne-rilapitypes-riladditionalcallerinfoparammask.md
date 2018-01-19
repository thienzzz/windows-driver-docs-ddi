---
UID : NE:rilapitypes.RILADDITIONALCALLERINFOPARAMMASK
title : RILADDITIONALCALLERINFOPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\riladditionalcallerinfoparammask_2.htm
old-project : netvista
ms.assetid : 1de91e12-1f8c-48fa-85e4-c3cb061fce78
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILADDITIONALCALLERINFOPARAMMASK, RILADDITIONALCALLERINFOPARAMMASK
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
req.alt-api : RILADDITIONALCALLERINFOPARAMMASK
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
req.typenames : RILADDITIONALCALLERINFOPARAMMASK
req.product : Windows 10 or later.
---

# RILADDITIONALCALLERINFOPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILADDITIONALCALLERINFOPARAMMASK { 
  RIL_PARAM_ADDTLCI_CALLID,
  RIL_PARAM_ADDTLCI_CALLERINFOLENGTH,
  RIL_PARAM_ADDTLCI_CALLERINFO,
  RIL_PARAM_ADDTLCI_ALL
} RILADDITIONALCALLERINFOPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_ADDTLCI_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_ADDTLCI_CALLERINFO</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_ADDTLCI_CALLERINFOLENGTH</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_ADDTLCI_CALLID</td>
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