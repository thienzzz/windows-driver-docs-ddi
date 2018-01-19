---
UID : NE:fwpsk.FWPS_FIELDS_RPC_EPMAP_
title : FWPS_FIELDS_RPC_EPMAP_
author : windows-driver-content
description : The FWPS_FIELDS_RPC_EPMAP enumeration type specifies the data field identifiers for the FWPS_LAYER_RPC_EPMAP run-time filtering layer.
old-location : netvista\fwps_fields_rpc_epmap.htm
old-project : netvista
ms.assetid : 78960e0c-6b27-4331-a0e0-3f7ba13a54cf
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FWPS_FIELDS_RPC_EPMAP_, FWPS_FIELDS_RPC_EPMAP
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Supported starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FWPS_FIELDS_RPC_EPMAP
req.alt-loc : fwpsk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : FWPS_FIELDS_RPC_EPMAP
---

# FWPS_FIELDS_RPC_EPMAP_ Enumeration
The FWPS_FIELDS_RPC_EPMAP enumeration type specifies the data field identifiers for the
  FWPS_LAYER_RPC_EPMAP 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layer</a>.

## Syntax
````
typedef enum FWPS_FIELDS_RPC_EPMAP_ { 
  FWPS_FIELD_RPC_EPMAP_REMOTE_USER_TOKEN,
  FWPS_FIELD_RPC_EPMAP_IF_UUID,
  FWPS_FIELD_RPC_EPMAP_IF_VERSION,
  FWPS_FIELD_RPC_EPMAP_PROTOCOL,
  FWPS_FIELD_RPC_EPMAP_AUTH_TYPE,
  FWPS_FIELD_RPC_EPMAP_AUTH_LEVEL,
  FWPS_FIELD_RPC_EPMAP_SEC_ENCRYPT_ALGORITHM,
  FWPS_FIELD_RPC_EPMAP_SEC_KEY_SIZE,
  FWPS_FIELD_RPC_EPMAP_LOCAL_ADDR_V4,
  FWPS_FIELD_RPC_EPMAP_LOCAL_ADDR_V6,
  FWPS_FIELD_RPC_EPMAP_LOCAL_PORT,
  FWPS_FIELD_RPC_EPMAP_PIPE,
  FWPS_FIELD_RPC_EPMAP_REMOTE_ADDR_V4,
  FWPS_FIELD_RPC_EPMAP_REMOTE_ADDR_V6,
  FWPS_FIELD_RPC_EPMAP_MAX
} FWPS_FIELDS_RPC_EPMAP;
````

## Constants

<table>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_AUTH_LEVEL</td>
<td>The authentication service level. For more information about authentication service levels, see
     Authentication-Service Constants in the RPC section of the Windows SDK documentation.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_AUTH_TYPE</td>
<td>The authentication service type. For more information about authentication service types, see
     Authentication-Service Constants in the RPC section of the Microsoft Windows SDK documentation.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_IF_UUID</td>
<td>The UUID of the RPC interface.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_IF_VERSION</td>
<td>The version of the RPC interface.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_LOCAL_ADDR_V4</td>
<td>The local IPv4 address.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_LOCAL_ADDR_V6</td>
<td>The local IPv6 address.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_LOCAL_PORT</td>
<td>The local transport protocol port number.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_MAX</td>
<td>The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_PIPE</td>
<td>The name of the remote named pipe.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_PROTOCOL</td>
<td></td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_REMOTE_ADDR_V4</td>
<td>The remote IPv4 address.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_REMOTE_ADDR_V6</td>
<td>The remote IPv6 address.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_REMOTE_USER_TOKEN</td>
<td>The identification of the remote user.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_SEC_ENCRYPT_ALGORITHM</td>
<td>The certificate-based security service provider interface (SSPI) encryption algorithm.</td>
</tr>

<tr>
<td>FWPS_FIELD_RPC_EPMAP_SEC_KEY_SIZE</td>
<td>The certificate-based SSPI encryption key size.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |