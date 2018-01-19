---
UID : NE:portcls._PC_EXIT_LATENCY
title : _PC_EXIT_LATENCY
author : windows-driver-content
description : This topic discusses the PC_EXIT_LATENCY enum, and describes its members. The latency times map to specific maximum times in which the device must be able to exit its sleep state and enter the fully functional state (D0).
old-location : audio\pc_exit_latency.htm
old-project : audio
ms.assetid : 9D1DA7D6-4200-4B5A-9EA5-0455DF56D6D8
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _PC_EXIT_LATENCY, PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : portcls.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PC_EXIT_LATENCY
req.alt-loc : Portcls.h
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
req.typenames : PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# _PC_EXIT_LATENCY Enumeration
This topic discusses the PC_EXIT_LATENCY enum, and describes its members. The latency times map to specific maximum times in which the device must be able to exit its sleep state and enter the fully functional state (D0).

## Syntax
````
typedef enum _PC_EXIT_LATENCY { 
  PcExitLatencyInstant     = 0,
  PcExitLatencyFast,
  PcExitLatencyResponsive
} PC_EXIT_LATENCY;
````

## Constants

<table>

<tr>
<td>PcExitLatencyFast</td>
<td>Indicates a 35-millisecond resume latency.</td>
</tr>

<tr>
<td>PcExitLatencyInstant</td>
<td>Indicates a 0-millisecond latency. This means "Do not power down" and it  will only be sent when a device is in the D0 state.</td>
</tr>

<tr>
<td>PcExitLatencyResponsive</td>
<td>Indicates a 300-millisecond resume latency.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | portcls.h |