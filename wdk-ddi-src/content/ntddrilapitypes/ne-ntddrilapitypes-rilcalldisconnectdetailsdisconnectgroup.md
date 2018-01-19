---
UID : NE:ntddrilapitypes.RILCALLDISCONNECTDETAILSDISCONNECTGROUP
title : RILCALLDISCONNECTDETAILSDISCONNECTGROUP
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcalldisconnectdetailsdisconnectgroup.htm
old-project : netvista
ms.assetid : d546e936-f8c6-45ad-8027-a8495b4633dc
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLDISCONNECTDETAILSDISCONNECTGROUP, RILCALLDISCONNECTDETAILSDISCONNECTGROUP
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
req.alt-api : RILCALLDISCONNECTDETAILSDISCONNECTGROUP
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
req.typenames : RILCALLDISCONNECTDETAILSDISCONNECTGROUP
---

# RILCALLDISCONNECTDETAILSDISCONNECTGROUP Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILCALLDISCONNECTDETAILSDISCONNECTGROUP { 
  RIL_CD_AS_CAUSE,
  RIL_CD_3GPP_NETWORK_CAUSE,
  RIL_CD_3GPP2_VENDOR_CAUSE,
  RIL_CD_OTHER_CAUSE,
  RIL_CD_3GPP_REJECT_CAUSE,
  RIL_CD_IMS_SIP_CAUSE,
  RIL_CD_CAUSE_MAX
} RILCALLDISCONNECTDETAILSDISCONNECTGROUP;
````

## Constants

<table>

<tr>
<td>RIL_CD_3GPP_NETWORK_CAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_CD_3GPP_REJECT_CAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_CD_3GPP2_VENDOR_CAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_CD_AS_CAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_CD_CAUSE_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_CD_IMS_SIP_CAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_CD_OTHER_CAUSE</td>
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