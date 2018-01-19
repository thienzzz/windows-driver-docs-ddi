---
UID : NE:fwpsk.FWPS_FIELDS_KM_AUTHORIZATION_
title : FWPS_FIELDS_KM_AUTHORIZATION_
author : windows-driver-content
description : The FWPS_FIELDS_KM_AUTHORIZATION enumeration type specifies the data field identifiers for the FWPS_LAYER_KM_AUTHORIZATION run-time filtering layer.
old-location : netvista\fwps_fields_km_authorization.htm
old-project : netvista
ms.assetid : c15ed590-4a7f-4f21-8e6e-1440a57b5659
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FWPS_FIELDS_KM_AUTHORIZATION_, FWPS_FIELDS_KM_AUTHORIZATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Supported starting with Windows 7.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FWPS_FIELDS_KM_AUTHORIZATION
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
req.typenames : FWPS_FIELDS_KM_AUTHORIZATION
---

# FWPS_FIELDS_KM_AUTHORIZATION_ Enumeration
The FWPS_FIELDS_KM_AUTHORIZATION enumeration type specifies the data field identifiers for the
  FWPS_LAYER_KM_AUTHORIZATION 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layer</a>.

## Syntax
````
typedef enum FWPS_FIELDS_KM_AUTHORIZATION_ { 
  FWPS_FIELD_KM_AUTHORIZATION_REMOTE_ID,
  FWPS_FIELD_KM_AUTHORIZATION_AUTHENTICATION_TYPE,
  FWPS_FIELD_KM_AUTHORIZATION_KM_TYPE,
  FWPS_FIELD_KM_AUTHORIZATION_DIRECTION,
  FWPS_FIELD_KM_AUTHORIZATION_KM_MODE,
  FWPS_FIELD_KM_AUTHORIZATION_IPSEC_POLICY_KEY,
  FWPS_FIELD_KM_AUTHORIZATION_NAP_CONTEXT,
  FWPS_FIELD_KM_AUTHORIZATION_MAX
} FWPS_FIELDS_KM_AUTHORIZATION;
````

## Constants

<table>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_AUTHENTICATION_TYPE</td>
<td>The type of authentication used.</td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_DIRECTION</td>
<td></td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_IPSEC_POLICY_KEY</td>
<td>The associated IPsec policy key.</td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_KM_MODE</td>
<td>The authorization mode.</td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_KM_TYPE</td>
<td>The type of Keying Module (KM) used.</td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_MAX</td>
<td>The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.</td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_NAP_CONTEXT</td>
<td>The Network Access Protection (NAP) certificate context.</td>
</tr>

<tr>
<td>FWPS_FIELD_KM_AUTHORIZATION_REMOTE_ID</td>
<td>The peer's identifier. This can be the User or Machine Token depending on the type, auth type, and
     mode.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |