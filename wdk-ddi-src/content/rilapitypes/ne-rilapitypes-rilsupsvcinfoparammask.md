---
UID : NE:rilapitypes.RILSUPSVCINFOPARAMMASK
title : RILSUPSVCINFOPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilsupsvcinfoparammask_2.htm
old-project : netvista
ms.assetid : 52dd2092-939a-491b-af2d-2ea86eabf99a
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILSUPSVCINFOPARAMMASK, RILSUPSVCINFOPARAMMASK
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
req.alt-api : RILSUPSVCINFOPARAMMASK
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
req.typenames : RILSUPSVCINFOPARAMMASK
req.product : Windows 10 or later.
---

# RILSUPSVCINFOPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILSUPSVCINFOPARAMMASK { 
  RIL_PARAM_SSI_FROM_NETWORK,
  RIL_PARAM_SSI_FAILURE_REASON,
  RIL_PARAM_SSI_SUPSVC_ACTION,
  RIL_PARAM_SSI_SUPSVC_TYPE,
  RIL_PARAM_SSI_CALL_FORWARDING_REASON,
  RIL_PARAM_SSI_CALL_BARRING_TYPE,
  RIL_PARAM_SSI_INFOCLASSES,
  RIL_PARAM_SSI_ALPHA_IDENTIFIER,
  RIL_PARAM_SSI_CALL_BARRING_PASSWORD,
  RIL_PARAM_SSI_NEW_CALL_BARRING_PASSWORD,
  RIL_PARAM_SSI_CALL_FORWARDING_SETTINGS,
  RIL_PARAM_SSI_CALLER_ID_SETTINGS,
  RIL_PARAM_SSI_DIALED_ID_SETTINGS,
  RIL_PARAM_SSI_HIDE_ID_SETTINGS,
  RIL_PARAM_SSI_CONNECTED_ID_SETTINGS,
  RIL_PARAM_SSI_SUPSERVICE_DATA,
  RIL_PARAM_SSI_ALL
} RILSUPSVCINFOPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_SSI_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_ALPHA_IDENTIFIER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_CALL_BARRING_PASSWORD</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_CALL_BARRING_TYPE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_CALL_FORWARDING_REASON</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_CALL_FORWARDING_SETTINGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_CALLER_ID_SETTINGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_CONNECTED_ID_SETTINGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_DIALED_ID_SETTINGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_FAILURE_REASON</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_FROM_NETWORK</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_HIDE_ID_SETTINGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_INFOCLASSES</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_NEW_CALL_BARRING_PASSWORD</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_SUPSERVICE_DATA</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_SUPSVC_ACTION</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_SSI_SUPSVC_TYPE</td>
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