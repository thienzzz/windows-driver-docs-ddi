---
UID : NE:wditypes._WDI_DATA_RATE_FLAGS
title : _WDI_DATA_RATE_FLAGS
author : windows-driver-content
description : The WDI_DATA_RATE_FLAGS enumeration defines the data rate flags.
old-location : netvista\wdi_data_rate_flags.htm
old-project : netvista
ms.assetid : 937D1C48-AC5A-4D55-8722-BDC1192613A9
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDI_DATA_RATE_FLAGS, WDI_DATA_RATE_FLAGS
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
req.alt-api : WDI_DATA_RATE_FLAGS
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
req.typenames : WDI_DATA_RATE_FLAGS
req.product : Windows 10 or later.
---

# _WDI_DATA_RATE_FLAGS Enumeration
The WDI_DATA_RATE_FLAGS enumeration defines the data rate flags.

## Syntax
````
typedef enum _WDI_DATA_RATE_FLAGS { 
  WDI_DATA_RATE_NON_STANDARD  = 0x01,
  WDI_DATA_RATE_RX_RATE       = 0x02,
  WDI_DATA_RATE_TX_RATE       = 0x04
} WDI_DATA_RATE_FLAGS;
````

## Constants

<table>

<tr>
<td>WDI_DATA_RATE_NON_STANDARD</td>
<td>The data rate is not a standard data rate defined in the IEEE 802.11 standards.</td>
</tr>

<tr>
<td>WDI_DATA_RATE_RX_RATE</td>
<td>The data rate can be used for RX.</td>
</tr>

<tr>
<td>WDI_DATA_RATE_TX_RATE</td>
<td>The data rate can be used for TX.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wditypes.hpp |