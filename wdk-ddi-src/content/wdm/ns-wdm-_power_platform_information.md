---
UID : NS:wdm._POWER_PLATFORM_INFORMATION
title : _POWER_PLATFORM_INFORMATION
author : windows-driver-content
description : The POWER_PLATFORM_INFORMATION structure contains information about the power capabilities of the system.
old-location : kernel\power_platform_information.htm
old-project : kernel
ms.assetid : 0E62B57D-F9B1-4B01-A19E-9E2DBC387578
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _POWER_PLATFORM_INFORMATION, POWER_PLATFORM_INFORMATION, *PPOWER_PLATFORM_INFORMATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : wdm.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : POWER_PLATFORM_INFORMATION
req.alt-loc : Wdm.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL (see Remarks section)
req.typenames : POWER_PLATFORM_INFORMATION, *PPOWER_PLATFORM_INFORMATION
req.product : Windows 10 or later.
---

# _POWER_PLATFORM_INFORMATION structure
The <b>POWER_PLATFORM_INFORMATION</b> structure contains information about  the power capabilities of the system.

## Syntax
````
typedef struct _POWER_PLATFORM_INFORMATION {
  BOOLEAN AoAc;
} POWER_PLATFORM_INFORMATION, *PPOWER_PLATFORM_INFORMATION;
````

## Members

        
            `AoAc`

            Indicates whether the system supports the connected standby power model.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h |