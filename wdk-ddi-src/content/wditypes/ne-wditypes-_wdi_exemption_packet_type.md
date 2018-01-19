---
UID : NE:wditypes._WDI_EXEMPTION_PACKET_TYPE
title : _WDI_EXEMPTION_PACKET_TYPE
author : windows-driver-content
description : The WDI_EXEMPTION_PACKET_TYPE enumeration defines the types of packet exemptions.
old-location : netvista\wdi_exemption_packet_type.htm
old-project : netvista
ms.assetid : 7F584EBE-9ACB-4AC7-9472-34322F24EF74
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDI_EXEMPTION_PACKET_TYPE, WDI_EXEMPTION_PACKET_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wditypes.hpp
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WDI_EXEMPTION_PACKET_TYPE
req.alt-loc : wditypes.hpp
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
req.typenames : WDI_EXEMPTION_PACKET_TYPE
req.product : Windows 10 or later.
---

# _WDI_EXEMPTION_PACKET_TYPE Enumeration
The WDI_EXEMPTION_PACKET_TYPE enumeration defines the types of packet exemptions.

## Syntax
````
typedef enum _WDI_EXEMPTION_PACKET_TYPE { 
  WDI_EXEMPT_PACKET_TYPE_UNICAST    = 1,
  WDI_EXEMPT_PACKET_TYPE_MULTICAST  = 2,
  WDI_EXEMPT_PACKET_TYPE_BOTH       = 3
} WDI_EXEMPTION_PACKET_TYPE;
````

## Constants

<table>

<tr>
<td>WDI_EXEMPT_PACKET_TYPE_BOTH</td>
<td>Exempt all packet types.</td>
</tr>

<tr>
<td>WDI_EXEMPT_PACKET_TYPE_MULTICAST</td>
<td>Exempt multicast and broadcast packets only.</td>
</tr>

<tr>
<td>WDI_EXEMPT_PACKET_TYPE_UNICAST</td>
<td>Exempt unicast packets only.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wditypes.hpp |