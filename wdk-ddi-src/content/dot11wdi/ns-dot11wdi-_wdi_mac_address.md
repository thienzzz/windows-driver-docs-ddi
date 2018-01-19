---
UID : NS:dot11wdi._WDI_MAC_ADDRESS
title : _WDI_MAC_ADDRESS
author : windows-driver-content
description : The WDI_MAC_ADDRESS structure defines an IEEE media access control (MAC) address.
old-location : netvista\wdi_mac_address.htm
old-project : netvista
ms.assetid : e170b797-f8bb-4d3c-a3ee-5fd1a817a500
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDI_MAC_ADDRESS, *PWDI_MAC_ADDRESS, WDI_MAC_ADDRESS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : dot11wdi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WDI_MAC_ADDRESS
req.alt-loc : dot11wdi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : "*PWDI_MAC_ADDRESS, WDI_MAC_ADDRESS"
---

# _WDI_MAC_ADDRESS structure
The 
  WDI_MAC_ADDRESS structure defines an IEEE media access control (MAC) address.

## Syntax
````
typedef struct _WDI_MAC_ADDRESS {
  UINT8 Address[6];
} WDI_MAC_ADDRESS, *PWDI_MAC_ADDRESS;
````

## Members

        
            `Address`

            A Wi-Fi MAC address.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dot11wdi.h |