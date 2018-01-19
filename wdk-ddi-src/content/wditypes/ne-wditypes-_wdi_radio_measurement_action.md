---
UID : NE:wditypes._WDI_RADIO_MEASUREMENT_ACTION
title : _WDI_RADIO_MEASUREMENT_ACTION
author : windows-driver-content
description : The WDI_RADIO_MEASUREMENT_ACTION enumeration defines the radio measurement actions.
old-location : netvista\wdi_radio_measurement_action.htm
old-project : netvista
ms.assetid : AA17E666-5934-453D-B55D-98F8616F6369
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDI_RADIO_MEASUREMENT_ACTION, WDI_RADIO_MEASUREMENT_ACTION
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
req.alt-api : WDI_RADIO_MEASUREMENT_ACTION
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
req.typenames : WDI_RADIO_MEASUREMENT_ACTION
req.product : Windows 10 or later.
---

# _WDI_RADIO_MEASUREMENT_ACTION Enumeration
The WDI_RADIO_MEASUREMENT_ACTION enumeration defines the radio measurement actions.

## Syntax
````
typedef enum _WDI_RADIO_MEASUREMENT_ACTION { 
  WDI_RADIO_MEASUREMENT_ACTION_NEIGHBOR_REPORT_REQUEST   = 4,
  WDI_RADIO_MEASUREMENT_ACTION_NEIGHBOR_REPORT_RESPONSE  = 5
} WDI_RADIO_MEASUREMENT_ACTION;
````

## Constants

<table>

<tr>
<td>WDI_RADIO_MEASUREMENT_ACTION_NEIGHBOR_REPORT_REQUEST</td>
<td>This refers to the neighbor report request action frame sent by the client to the AP.</td>
</tr>

<tr>
<td>WDI_RADIO_MEASUREMENT_ACTION_NEIGHBOR_REPORT_RESPONSE</td>
<td>This refers to the neighbor report response action frame from the AP.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wditypes.hpp |