---
UID : NE:ntddrilapitypes.RILMESSAGEPARAMMASK
title : RILMESSAGEPARAMMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmessageparammask.htm
old-project : netvista
ms.assetid : 718c9d10-fd89-4d31-815e-da4dea0a3f34
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMESSAGEPARAMMASK, RILMESSAGEPARAMMASK
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
req.alt-api : RILMESSAGEPARAMMASK
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
req.typenames : RILMESSAGEPARAMMASK
---

# RILMESSAGEPARAMMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILMESSAGEPARAMMASK { 
  RIL_PARAM_M_TYPE,
  RIL_PARAM_M_FLAGS,
  RIL_PARAM_M_ORIGADDRESS,
  RIL_PARAM_M_TGTRECIPADDRESS,
  RIL_PARAM_M_DESTADDRESS,
  RIL_PARAM_M_SCRECEIVETIME,
  RIL_PARAM_M_TGTSCRECEIVETIME,
  RIL_PARAM_M_TGTDISCHARGETIME,
  RIL_PARAM_M_PROTOCOLID,
  RIL_PARAM_M_DATACODING,
  RIL_PARAM_M_TGTDLVSTATUS,
  RIL_PARAM_M_VPFORMAT,
  RIL_PARAM_M_VP,
  RIL_PARAM_M_GEOSCOPE,
  RIL_PARAM_M_MSGCODE,
  RIL_PARAM_M_UPDATENUMBER,
  RIL_PARAM_M_ID,
  RIL_PARAM_M_TOTALPAGES,
  RIL_PARAM_M_PAGENUMBER,
  RIL_PARAM_M_HDRLENGTH,
  RIL_PARAM_M_SERIALNUMBER,
  RIL_PARAM_M_MSGLENGTH,
  RIL_PARAM_M_HDR,
  RIL_PARAM_M_MSG,
  RIL_PARAM_M_WARNINGTYPE,
  RIL_PARAM_M_EUSERALERT,
  RIL_PARAM_M_POPUP,
  RIL_PARAM_M_MSGID,
  RIL_PARAM_M_ORIGSUBADDRESS,
  RIL_PARAM_M_DESTSUBADDRESS,
  RIL_PARAM_M_DIGIT,
  RIL_PARAM_M_PRIVACY,
  RIL_PARAM_M_PRIORITY,
  RIL_PARAM_M_TELESERVICE,
  RIL_PARAM_M_LANG,
  RIL_PARAM_M_VALIDITYPERIODABS,
  RIL_PARAM_M_VALIDITYPERIODREL,
  RIL_PARAM_M_DEFERREDDELTIMEABS,
  RIL_PARAM_M_DEFERREDDELTIMEREL,
  RIL_PARAM_M_ENCODING,
  RIL_PARAM_M_USERRESPONSECODE,
  RIL_PARAM_M_DISPLAYMODE,
  RIL_PARAM_M_CALLBACKNUM,
  RIL_PARAM_M_NUMMSGS,
  RIL_PARAM_M_CAUSECODE,
  RIL_PARAM_M_REPLYSEQNUMBER,
  RIL_PARAM_M_SERVICEID,
  RIL_PARAM_M_USERACK,
  RIL_PARAM_M_DELIVERYACK,
  RIL_PARAM_M_ALERTONMSGDELIVERY,
  RIL_PARAM_M_HDRLENGTHCDMA,
  RIL_PARAM_M_MSGSTATUSTYPE,
  RIL_PARAM_M_BEARERREPLYACK,
  RIL_PARAM_M_ALL_IN_DELIVER,
  RIL_PARAM_M_ALL_IN_STATUS,
  RIL_PARAM_M_ALL_OUT_SUBMIT,
  RIL_PARAM_M_ALL_BC_GENERAL,
  RIL_PARAM_M_ALL_IN_IS637DELIVER,
  RIL_PARAM_M_ALL_OUT_IS637SUBMIT,
  RIL_PARAM_M_ALL_IN_IS637STATUS,
  RIL_PARAM_M_ALL_OUT_IS637STATUS
} RILMESSAGEPARAMMASK;
````

## Constants

<table>

<tr>
<td>RIL_PARAM_M_ALERTONMSGDELIVERY</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_BC_GENERAL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_IN_DELIVER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_IN_IS637DELIVER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_IN_IS637STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_IN_STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_OUT_IS637STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_OUT_IS637SUBMIT</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ALL_OUT_SUBMIT</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_BEARERREPLYACK</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_CALLBACKNUM</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_CAUSECODE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DATACODING</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DEFERREDDELTIMEABS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DEFERREDDELTIMEREL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DELIVERYACK</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DESTADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DESTSUBADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DIGIT</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_DISPLAYMODE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ENCODING</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_EUSERALERT</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_FLAGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_GEOSCOPE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_HDR</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_HDRLENGTH</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_HDRLENGTHCDMA</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ID</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_LANG</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_MSG</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_MSGCODE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_MSGID</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_MSGLENGTH</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_MSGSTATUSTYPE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_NUMMSGS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ORIGADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_ORIGSUBADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_PAGENUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_POPUP</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_PRIORITY</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_PRIVACY</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_PROTOCOLID</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_REPLYSEQNUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_SCRECEIVETIME</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_SERIALNUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_SERVICEID</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TELESERVICE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TGTDISCHARGETIME</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TGTDLVSTATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TGTRECIPADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TGTSCRECEIVETIME</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TOTALPAGES</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_TYPE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_UPDATENUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_USERACK</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_USERRESPONSECODE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_VALIDITYPERIODABS</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_VALIDITYPERIODREL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_VP</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_VPFORMAT</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_M_WARNINGTYPE</td>
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