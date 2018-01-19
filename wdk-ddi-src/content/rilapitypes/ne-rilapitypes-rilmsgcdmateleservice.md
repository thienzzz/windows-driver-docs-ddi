---
UID : NE:rilapitypes.RILMSGCDMATELESERVICE
title : RILMSGCDMATELESERVICE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmsgcdmateleservice_2.htm
old-project : netvista
ms.assetid : 35d3e419-ad21-403d-8590-f49cf6fd3b25
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMSGCDMATELESERVICE, RILMSGCDMATELESERVICE
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
req.alt-api : RILMSGCDMATELESERVICE
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
req.typenames : RILMSGCDMATELESERVICE
req.product : Windows 10 or later.
---

# RILMSGCDMATELESERVICE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILMSGCDMATELESERVICE { 
  RIL_MSGTELESERVICE_MESSAGING_OLD,
  RIL_MSGTELESERVICE_VOICEMAIL_OLD,
  RIL_MSGTELESERVICE_WAP_OLD,
  RIL_MSGTELESERVICE_BROADCAST_OLD,
  RIL_MSGTELESERVICE_SELFREG_OLD,
  RIL_MSGTELESERVICE_PAGING,
  RIL_MSGTELESERVICE_MESSAGING,
  RIL_MSGTELESERVICE_WEMT,
  RIL_MSGTELESERVICE_VOICEMAIL_VMN_95,
  RIL_MSGTELESERVICE_VOICEMAIL_MWI,
  RIL_MSGTELESERVICE_WAP,
  RIL_MSGTELESERVICE_WAP_CT_MMS,
  RIL_MSGTELESERVICE_WAP_CT_OMA,
  RIL_MSGTELESERVICE_BROADCAST,
  RIL_MSGTELESERVICE_SELFREG
} RILMSGCDMATELESERVICE;
````

## Constants

<table>

<tr>
<td>RIL_MSGTELESERVICE_BROADCAST</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_BROADCAST_OLD</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_MESSAGING</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_MESSAGING_OLD</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_PAGING</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_SELFREG</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_SELFREG_OLD</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_VOICEMAIL_MWI</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_VOICEMAIL_OLD</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_VOICEMAIL_VMN_95</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_WAP</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_WAP_CT_MMS</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_WAP_CT_OMA</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_WAP_OLD</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGTELESERVICE_WEMT</td>
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