---
UID : NE:ntddrilapitypes.RILRILREGSTATUSINFOREJECTREASON
title : RILRILREGSTATUSINFOREJECTREASON
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilrilregstatusinforejectreason.htm
old-project : netvista
ms.assetid : 17aad504-4223-4764-8a24-536a81807650
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILRILREGSTATUSINFOREJECTREASON, RILRILREGSTATUSINFOREJECTREASON
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
req.alt-api : RILRILREGSTATUSINFOREJECTREASON
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
req.typenames : RILRILREGSTATUSINFOREJECTREASON
---

# RILRILREGSTATUSINFOREJECTREASON Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILRILREGSTATUSINFOREJECTREASON { 
  RIL_REGREJECTREASON_IMSIUNK_HLR,
  RIL_REGREJECTREASON_ILLEGAL_MS,
  RIL_REGREJECTREASON_IMSIUNK_VLR,
  RIL_REGREJECTREASON_IMSI_NOTACCEPTED,
  RIL_REGREJECTREASON_ILLEGAL_ME,
  RIL_REGREJECTREASON_PLMN_NOTALLOWED,
  RIL_REGREJECTREASON_LOCAREA_NOTALLOWED,
  RIL_REGREJECTREASON_ROAMING_NOTALLOWED,
  RIL_REGREJECTREASON_NOSUITABLECELL,
  RIL_REGREJECTREASON_NETWORKFAILURE,
  RIL_REGREJECTREASON_MACFAILURE,
  RIL_REGREJECTREASON_SYNCHFAILURE,
  RIL_REGREJECTREASON_CONGESTION,
  RIL_REGREJECTREASON_GSMAUTH_NOTACCEPTED,
  RIL_REGREJECTREASON_CSG_NOTAUTHORIZED,
  RIL_REGREJECTREASON_SVCOPT_NOTSUPPORTED,
  RIL_REGREJECTREASON_REQSVCOPT_NOTSUBSCRIBED,
  RIL_REGREJECTREASON_SVCOPT_OUTOFORDER
} RILRILREGSTATUSINFOREJECTREASON;
````

## Constants

<table>

<tr>
<td>RIL_REGREJECTREASON_CONGESTION</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_CSG_NOTAUTHORIZED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_GSMAUTH_NOTACCEPTED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_ILLEGAL_ME</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_ILLEGAL_MS</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_IMSI_NOTACCEPTED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_IMSIUNK_HLR</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_IMSIUNK_VLR</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_LOCAREA_NOTALLOWED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_MACFAILURE</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_NETWORKFAILURE</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_NOSUITABLECELL</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_PLMN_NOTALLOWED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_REQSVCOPT_NOTSUBSCRIBED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_ROAMING_NOTALLOWED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_SVCOPT_NOTSUPPORTED</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_SVCOPT_OUTOFORDER</td>
<td></td>
</tr>

<tr>
<td>RIL_REGREJECTREASON_SYNCHFAILURE</td>
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