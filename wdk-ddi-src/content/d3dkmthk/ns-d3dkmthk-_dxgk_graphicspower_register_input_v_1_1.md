---
UID : NS:d3dkmthk._DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1
title : _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1
author : windows-driver-content
description : Used to register the power state of a new input.
old-location : display\dxgk-graphicspower-register-input-v-1-1.htm
old-project : display
ms.assetid : 5b120f3c-43d2-447a-9959-0788d7decf50
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1, DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1, DXGK_GRAPHICSPOWER_REGISTER_INPUT, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmthk.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1
req.alt-loc : d3dkmthk.h
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
req.typenames : DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1
---

# _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1 structure
Used to register the power state of a new input.

## Syntax
````
typedef struct _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1 {
  ULONG                      Version;
  PVOID                      PrivateHandle;
  PDXGK_POWER_NOTIFICATION   PowerNotificationCb;
  PDXGK_REMOVAL_NOTIFICATION RemovalNotificationCb;
  PDXGK_FSTATE_NOTIFICATION  FStateNotificationCb;
} DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_1;
````

## Members

        
            `FStateNotificationCb`

            Issues a state notification.
        
            `PowerNotificationCb`

            Issues a power notification.
        
            `PrivateHandle`

            A private handle to the device.
        
            `RemovalNotificationCb`

            Issues a removal notification.
        
            `Version`

            The current version being used.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h |