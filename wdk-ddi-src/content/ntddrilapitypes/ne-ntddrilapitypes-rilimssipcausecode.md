---
UID : NE:ntddrilapitypes.RILIMSSIPCAUSECODE
title : RILIMSSIPCAUSECODE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilimssipcausecode.htm
old-project : netvista
ms.assetid : b76ea0fb-8139-4272-b9a0-2daa5b660c7d
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILIMSSIPCAUSECODE, RILIMSSIPCAUSECODE
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
req.alt-api : RILIMSSIPCAUSECODE
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
req.typenames : RILIMSSIPCAUSECODE
---

# RILIMSSIPCAUSECODE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILIMSSIPCAUSECODE { 
  RIL_IMSSIPCAUSE_UNAUTHORIZED,
  RIL_IMSSIPCAUSE_PAYMENT_REQUIRED,
  RIL_IMSSIPCAUSE_FORBIDDEN,
  RIL_IMSSIPCAUSE_NOT_FOUND,
  RIL_IMSSIPCAUSE_METHOD_NOT_ALLOWED,
  RIL_IMSSIPCAUSE_NOT_ACCEPTABLE,
  RIL_IMSSIPCAUSE_PROXY_AUTHENTICATION_REQUIRED,
  RIL_IMSSIPCAUSE_REQUEST_TIMEOUT,
  RIL_IMSSIPCAUSE_GONE,
  RIL_IMSSIPCAUSE_REQUEST_ENTITY_TOO_LARGE,
  RIL_IMSSIPCAUSE_REQUEST_URI_TOO_LONG,
  RIL_IMSSIPCAUSE_UNSUPPORTED_MEDIA_TYPE,
  RIL_IMSSIPCAUSE_UNSUPPORTED_URI_SCHEME,
  RIL_IMSSIPCAUSE_BAD_EXTENSION,
  RIL_IMSSIPCAUSE_EXTENSION_REQUIRED,
  RIL_IMSSIPCAUSE_INTERVAL_TOO_BRIEF,
  RIL_IMSSIPCAUSE_TEMPORARILY_UNAVAILABLE,
  RIL_IMSSIPCAUSE_CALL_OR_TRANSACTION_DOES_NOT_EXIST,
  RIL_IMSSIPCAUSE_LOOP_DETECTED,
  RIL_IMSSIPCAUSE_TOO_MANY_HOPS,
  RIL_IMSSIPCAUSE_ADDRESS_INCOMPLETE,
  RIL_IMSSIPCAUSE_AMBIGUOUS,
  RIL_IMSSIPCAUSE_BUSY_HERE,
  RIL_IMSSIPCAUSE_REQUEST_TERMINATED,
  RIL_IMSSIPCAUSE_NOT_ACCEPTABLE_HERE,
  RIL_IMSSIPCAUSE_REQUEST_PENDING,
  RIL_IMSSIPCAUSE_UNDECIPHERABLE,
  RIL_IMSSIPCAUSE_SERVER_INTERNAL_ERROR,
  RIL_IMSSIPCAUSE_NOT_IMPLEMENTED,
  RIL_IMSSIPCAUSE_BAD_GATEWAY,
  RIL_IMSSIPCAUSE_SERVICE_UNAVAILABLE,
  RIL_IMSSIPCAUSE_SERVER_TIMEOUT,
  RIL_IMSSIPCAUSE_VERSION_NOT_SUPPORTED,
  RIL_IMSSIPCAUSE_MESSAGE_TOO_LARGE,
  RIL_IMSSIPCAUSE_BUSY_EVERYWHERE,
  RIL_IMSSIPCAUSE_DECLINE,
  RIL_IMSSIPCAUSE_DOES_NOT_EXIST_ANYWHERE,
  RIL_IMSSIPCAUSE_NOT_ACCEPTABLE_PARTIAL
} RILIMSSIPCAUSECODE;
````

## Constants

<table>

<tr>
<td>RIL_IMSSIPCAUSE_ADDRESS_INCOMPLETE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_AMBIGUOUS</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_BAD_EXTENSION</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_BAD_GATEWAY</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_BUSY_EVERYWHERE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_BUSY_HERE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_CALL_OR_TRANSACTION_DOES_NOT_EXIST</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_DECLINE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_DOES_NOT_EXIST_ANYWHERE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_EXTENSION_REQUIRED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_FORBIDDEN</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_GONE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_INTERVAL_TOO_BRIEF</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_LOOP_DETECTED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_MESSAGE_TOO_LARGE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_METHOD_NOT_ALLOWED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_NOT_ACCEPTABLE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_NOT_ACCEPTABLE_HERE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_NOT_ACCEPTABLE_PARTIAL</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_NOT_FOUND</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_NOT_IMPLEMENTED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_PAYMENT_REQUIRED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_PROXY_AUTHENTICATION_REQUIRED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_REQUEST_ENTITY_TOO_LARGE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_REQUEST_PENDING</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_REQUEST_TERMINATED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_REQUEST_TIMEOUT</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_REQUEST_URI_TOO_LONG</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_SERVER_INTERNAL_ERROR</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_SERVER_TIMEOUT</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_SERVICE_UNAVAILABLE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_TEMPORARILY_UNAVAILABLE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_TOO_MANY_HOPS</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_UNAUTHORIZED</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_UNDECIPHERABLE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_UNSUPPORTED_MEDIA_TYPE</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_UNSUPPORTED_URI_SCHEME</td>
<td></td>
</tr>

<tr>
<td>RIL_IMSSIPCAUSE_VERSION_NOT_SUPPORTED</td>
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