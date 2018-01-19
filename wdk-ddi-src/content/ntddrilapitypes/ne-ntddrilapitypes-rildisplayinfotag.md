---
UID : NE:ntddrilapitypes.RILDISPLAYINFOTAG
title : RILDISPLAYINFOTAG
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rildisplayinfotag.htm
old-project : netvista
ms.assetid : ba47d9e3-4e95-479b-9e6a-10eb723e7d59
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILDISPLAYINFOTAG, RILDISPLAYINFOTAG
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
req.alt-api : RILDISPLAYINFOTAG
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
req.typenames : RILDISPLAYINFOTAG
---

# RILDISPLAYINFOTAG Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILDISPLAYINFOTAG { 
  RIL_EXTENDED_DISPLAY_TAG_SKIP,
  RIL_EXTENDED_DISPLAY_TAG_CONTINUATION,
  RIL_EXTENDED_DISPLAY_TAG_CALLED_ADDRESS,
  RIL_EXTENDED_DISPLAY_TAG_CAUSE,
  RIL_EXTENDED_DISPLAY_TAG_PROGRESS_INDICATOR,
  RIL_EXTENDED_DISPLAY_TAG_NOTIFICATION_INDICATOR,
  RIL_EXTENDED_DISPLAY_TAG_PROMPT,
  RIL_EXTENDED_DISPLAY_TAG_ACCUMULATED_DIGITS,
  RIL_EXTENDED_DISPLAY_TAG_STATUS,
  RIL_EXTENDED_DISPLAY_TAG_INBAND,
  RIL_EXTENDED_DISPLAY_TAG_CALLING_ADDRESS,
  RIL_EXTENDED_DISPLAY_TAG_REASON,
  RIL_EXTENDED_DISPLAY_TAG_CALLING_PARTY_NAME,
  RIL_EXTENDED_DISPLAY_TAG_CALLED_PARTY_NAME,
  RIL_EXTENDED_DISPLAY_TAG_ORIGINAL_CALLED_NAME,
  RIL_EXTENDED_DISPLAY_TAG_REDIRECTING_NAME,
  RIL_EXTENDED_DISPLAY_TAG_CONNECTED_NAME,
  RIL_EXTENDED_DISPLAY_TAG_ORIGINATING_RESTRICT,
  RIL_EXTENDED_DISPLAY_TAG_DATE_TIME_OF_DAY,
  RIL_EXTENDED_DISPLAY_TAG_CALL_APPEARANCE_ID,
  RIL_EXTENDED_DISPLAY_TAG_FEATURE_ADDRESS,
  RIL_EXTENDED_DISPLAY_TAG_REDIRECTION_NAME,
  RIL_EXTENDED_DISPLAY_TAG_REDIRECTION_NUMBER,
  RIL_EXTENDED_DISPLAY_TAG_REDIRECTING_NUMBER,
  RIL_EXTENDED_DISPLAY_TAG_ORIGINAL_CALLED_NUMBER,
  RIL_EXTENDED_DISPLAY_TAG_CONNECTED_NUMBER,
  RIL_EXTENDED_DISPLAY_TAG_TEXT,
  RIL_EXTENDED_DISPLAY_TAG_MAX
} RILDISPLAYINFOTAG;
````

## Constants

<table>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_ACCUMULATED_DIGITS</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CALL_APPEARANCE_ID</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CALLED_ADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CALLED_PARTY_NAME</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CALLING_ADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CALLING_PARTY_NAME</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CAUSE</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CONNECTED_NAME</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CONNECTED_NUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_CONTINUATION</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_DATE_TIME_OF_DAY</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_FEATURE_ADDRESS</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_INBAND</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_NOTIFICATION_INDICATOR</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_ORIGINAL_CALLED_NAME</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_ORIGINAL_CALLED_NUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_ORIGINATING_RESTRICT</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_PROGRESS_INDICATOR</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_PROMPT</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_REASON</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_REDIRECTING_NAME</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_REDIRECTING_NUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_REDIRECTION_NAME</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_REDIRECTION_NUMBER</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_SKIP</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_STATUS</td>
<td></td>
</tr>

<tr>
<td>RIL_EXTENDED_DISPLAY_TAG_TEXT</td>
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