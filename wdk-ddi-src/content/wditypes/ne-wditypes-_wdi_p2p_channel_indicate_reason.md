---
UID : NE:wditypes._WDI_P2P_CHANNEL_INDICATE_REASON
title : _WDI_P2P_CHANNEL_INDICATE_REASON
author : windows-driver-content
description : The WDI_P2P_CHANNEL_INDICATE_REASON enumeration defines Wi-Fi Direct channel indication reason values.
old-location : netvista\wdi_p2p_channel_indicate_reason.htm
old-project : netvista
ms.assetid : F6C2D044-E64B-4DA5-A168-20C99F325451
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDI_P2P_CHANNEL_INDICATE_REASON, WDI_P2P_CHANNEL_INDICATE_REASON
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
req.alt-api : WDI_P2P_CHANNEL_INDICATE_REASON
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
req.typenames : WDI_P2P_CHANNEL_INDICATE_REASON
req.product : Windows 10 or later.
---

# _WDI_P2P_CHANNEL_INDICATE_REASON Enumeration
The WDI_P2P_CHANNEL_INDICATE_REASON enumeration defines Wi-Fi Direct channel indication reason values.

## Syntax
````
typedef enum _WDI_P2P_CHANNEL_INDICATE_REASON { 
  WDI_P2P_CHANNEL_INDICATE_REASON_NEW_CONNECTION     = 0x0001,
  WDI_P2P_CHANNEL_INDICATE_REASON_ECSA_REQUESTED     = 0x0002,
  WDI_P2P_CHANNEL_INDICATE_REASON_ECSA_GO_INITIATED  = 0x0003
} WDI_P2P_CHANNEL_INDICATE_REASON;
````

## Constants

<table>

<tr>
<td>WDI_P2P_CHANNEL_INDICATE_REASON_ECSA_GO_INITIATED</td>
<td>eCSA initiated by GO.</td>
</tr>

<tr>
<td>WDI_P2P_CHANNEL_INDICATE_REASON_ECSA_REQUESTED</td>
<td>eCSA request from the peer.</td>
</tr>

<tr>
<td>WDI_P2P_CHANNEL_INDICATE_REASON_NEW_CONNECTION</td>
<td>New connection set up.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wditypes.hpp |