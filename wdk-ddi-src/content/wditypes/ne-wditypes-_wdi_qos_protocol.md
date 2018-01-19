---
UID : NE:wditypes._WDI_QOS_PROTOCOL
title : _WDI_QOS_PROTOCOL
author : windows-driver-content
description : The WDI_QOS_PROTOCOL enumeration defines Wi-Fi QOS protocols.
old-location : netvista\wdi_qos_protocol.htm
old-project : netvista
ms.assetid : 39466BF7-0517-4113-9C94-26D8691CCCC1
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDI_QOS_PROTOCOL, WDI_QOS_PROTOCOL
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
req.alt-api : WDI_QOS_PROTOCOL
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
req.typenames : WDI_QOS_PROTOCOL
req.product : Windows 10 or later.
---

# _WDI_QOS_PROTOCOL Enumeration
The WDI_QOS_PROTOCOL enumeration defines Wi-Fi QOS protocols.

## Syntax
````
typedef enum _WDI_QOS_PROTOCOL { 
  WDI_QOS_PROTOCOL_NONE  = 0x00,
  WDI_QOS_PROTOCOL_WMM   = 0x01,
  WDI_QOS_PROTOCOL_11E   = 0x02
} WDI_QOS_PROTOCOL;
````

## Constants

<table>

<tr>
<td>WDI_QOS_PROTOCOL_11E</td>
<td>802.11E</td>
</tr>

<tr>
<td>WDI_QOS_PROTOCOL_NONE</td>
<td>None</td>
</tr>

<tr>
<td>WDI_QOS_PROTOCOL_WMM</td>
<td>Wi-Fi Multimedia (WMM, formerly known as Wireless Multimedia Extensions)</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wditypes.hpp |