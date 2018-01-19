---
UID : NE:fwpsk.FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
title : FWPS_FIELDS_ALE_AUTH_LISTEN_V6_
author : windows-driver-content
description : The FWPS_FIELDS_ALE_AUTH_LISTEN_V6 enumeration type specifies the data field identifiers for the FWPS_LAYER_ALE_AUTH_LISTEN_V6 and FWPS_LAYER_ALE_AUTH_LISTEN_V6_DISCARD run-time filtering layers
old-location : netvista\fwps_fields_ale_auth_listen_v6.htm
old-project : netvista
ms.assetid : 8225be6d-b7a4-44db-bdff-bc223aa213c5
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FWPS_FIELDS_ALE_AUTH_LISTEN_V6_, FWPS_FIELDS_ALE_AUTH_LISTEN_V6
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Unless otherwise noted, supported starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FWPS_FIELDS_ALE_AUTH_LISTEN_V6
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
req.typenames : FWPS_FIELDS_ALE_AUTH_LISTEN_V6
---

# FWPS_FIELDS_ALE_AUTH_LISTEN_V6_ Enumeration
The FWPS_FIELDS_ALE_AUTH_LISTEN_V6 enumeration type specifies the data field identifiers for the
  FWPS_LAYER_ALE_AUTH_LISTEN_V6 and FWPS_LAYER_ALE_AUTH_LISTEN_V6_DISCARD 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layers</a>

## Syntax
````
typedef enum FWPS_FIELDS_ALE_AUTH_LISTEN_V6_ { 
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_APP_ID,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_USER_ID,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_ADDRESS,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_ADDRESS_TYPE,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_PORT,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_INTERFACE,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_FLAGS,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_INTERFACE_TYPE,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_TUNNEL_TYPE,
#if (NTDDI_VERSION >= NTDDI_WIN7)
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_LOCAL_INTERFACE_PROFILE_ID,
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_SIO_FIREWALL_SOCKET_PROPERTY,
#if (NTDDI_VERSION >= NTDDI_WIN8)
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_PACKAGE_ID,
#endif 
#endif 
  FWPS_FIELD_ALE_AUTH_LISTEN_V6_MAX
} FWPS_FIELDS_ALE_AUTH_LISTEN_V6;
````

## Constants

<table>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_APP_ID</td>
<td>The full path of the application.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_PACKAGE_ID</td>
<td>The package identifier is a security identifier (SID) that identifies the associated AppContainer process. For more information about the SID structure, see the description for the SID structure in the Microsoft Windows SDK documentation.

<div class="alert"><b>Note</b>  Supported starting with Windows 8.</div>
<div> </div></td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_ALE_USER_ID</td>
<td>The identifier of the local user.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_FLAGS</td>
<td>A bitwise OR of a combination of filtering condition flags. For information about the possible
     flags, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff549942">Filtering Condition Flags</a>.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_INTERFACE_TYPE</td>
<td>The type of the network interface, as defined by the Internet Assigned Numbers Authority (IANA).
     For more information, see 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=60066">IANAifType-MIB Definitions</a>.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_ADDRESS</td>
<td>The local IP address.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_ADDRESS_TYPE</td>
<td>The local IP address type. The possible values are defined by the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a> enumeration.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_INTERFACE</td>
<td>The locally unique identifier (<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>) for the network interface associated with the
     local IP address.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_IP_LOCAL_PORT</td>
<td>The local transport protocol port number.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_LOCAL_INTERFACE_PROFILE_ID</td>
<td>The profile identifier (network category) of the network interface associated with the local IP
     address. The possible network category values are: public (1), private (2), or domain (3).
     

<div class="alert"><b>Note</b>  Supported starting with Windows 7.</div>
<div> </div></td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_MAX</td>
<td>The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.</td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_SIO_FIREWALL_SOCKET_PROPERTY</td>
<td>The IP_PROTECTION_LEVEL property associated with the socket.
     

<div class="alert"><b>Note</b>  Supported starting with Windows 7.</div>
<div> </div></td>
</tr>

<tr>
<td>FWPS_FIELD_ALE_AUTH_LISTEN_V6_TUNNEL_TYPE</td>
<td>The encapsulation method used by a tunnel if the 
     <b>IfType</b> member of the IP_ADAPTER_ADDRESSES structure is IF_TYPE_TUNNEL. The tunnel type is defined
     by IANA. For more information, see 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=60066">IANAifType-MIB Definitions</a> and the
     Windows SDK.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |

## See Also

<dl>
<dt>
<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_FIELDS_ALE_AUTH_LISTEN_V6 enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>