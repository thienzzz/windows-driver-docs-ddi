---
UID : NE:rilapitypes.RILCALLINFOPARAMMASK
title : RILCALLINFOPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallinfoparammask_2.htm
old-project : netvista
ms.assetid : 8e5935d9-382f-409d-a9ed-9381613b5d9c
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLINFOPARAMMASK, RILCALLINFOPARAMMASK
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
req.alt-api : RILCALLINFOPARAMMASK
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
req.typenames : RILCALLINFOPARAMMASK
req.product : Windows 10 or later.
---

# RILCALLINFOPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLINFOPARAMMASK { 
  RIL_PARAM_CI_ID,
  RIL_PARAM_CI_DIRECTION,
  RIL_PARAM_CI_STATUS,
  RIL_PARAM_CI_TYPE,
  RIL_PARAM_CI_MULTIPARTY,
  RIL_PARAM_CI_ADDRESS,
  RIL_PARAM_CI_SUBADDRESS,
  RIL_PARAM_CI_DESCRIPTION,
  RIL_PARAM_CI_NUM_PRES_IND,
  RIL_PARAM_CI_NAME_PRES_IND,
  RIL_PARAM_CI_FLAGS,
  RIL_PARAM_CI_DISCONNECTINITIATOR,
  RIL_PARAM_CI_DISCONNECTREASON,
  RIL_PARAM_CI_DISCONNECTDETAILS,
  RIL_PARAM_CI_OFFERANSWER,
  RIL_PARAM_CI_HANDOVERSTATE,
  RIL_PARAM_CI_CALLMODIFICATIONCAUSE,
  RIL_PARAM_CI_RTTMODETYPE,
  RIL_PARAM_CI_RTTCAPINFO,
  RIL_PARAM_CI_RTTACTION,
  RIL_PARAM_CI_ALL
} RILCALLINFOPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_CI_ADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_CALLMODIFICATIONCAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_DESCRIPTION</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_DIRECTION</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_DISCONNECTDETAILS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_DISCONNECTINITIATOR</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_DISCONNECTREASON</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_FLAGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_HANDOVERSTATE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_ID</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_MULTIPARTY</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_NAME_PRES_IND</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_NUM_PRES_IND</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_OFFERANSWER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_RTTACTION</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_RTTCAPINFO</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_RTTMODETYPE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_SUBADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_CI_TYPE</td>
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