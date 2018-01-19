---
UID : NE:rilapitypes.RILMSGCDMAMSGENCODING
title : RILMSGCDMAMSGENCODING
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmsgcdmamsgencoding_2.htm
old-project : netvista
ms.assetid : 85586f69-09c3-4ebe-ad90-eb1b18e9d552
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMSGCDMAMSGENCODING, RILMSGCDMAMSGENCODING
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
req.alt-api : RILMSGCDMAMSGENCODING
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
req.typenames : RILMSGCDMAMSGENCODING
req.product : Windows 10 or later.
---

# RILMSGCDMAMSGENCODING Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILMSGCDMAMSGENCODING { 
  RIL_MSGCODING_7BITASCII,
  RIL_MSGCODING_UNICODE,
  RIL_MSGCODING_7BITGSM,
  RIL_MSGCODING_8BITGSM,
  RIL_MSGCODING_OCTET,
  RIL_MSGCODING_IA5,
  RIL_MSGCODING_JIS,
  RIL_MSGCODING_KOREAN,
  RIL_MSGCODING_LATIN_HEBREW,
  RIL_MSGCODING_LATIN,
  RIL_MSGCODING_MAX
} RILMSGCDMAMSGENCODING;
````

## Constants

<table>

<tr>
<td>RIL_MSGCODING_7BITASCII</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_7BITGSM</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_8BITGSM</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_IA5</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_JIS</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_KOREAN</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_LATIN</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_LATIN_HEBREW</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_MAX</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_OCTET</td>
<td></td>
</tr>

<tr>
<td>RIL_MSGCODING_UNICODE</td>
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