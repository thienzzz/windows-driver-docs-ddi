---
UID : NS:ntddrilapitypes.RILSIGNALQUALITY
title : RILSIGNALQUALITY
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilsignalquality.htm
old-project : netvista
ms.assetid : b2edfcdb-28b9-4322-8bfb-4d5d2c2d1519
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILSIGNALQUALITY, RILSIGNALQUALITY, *LPRILSIGNALQUALITY
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddrilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILSIGNALQUALITY
req.alt-loc : ntddrilapitypes.h
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
req.typenames : RILSIGNALQUALITY, *LPRILSIGNALQUALITY
---

# RILSIGNALQUALITY structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILSIGNALQUALITY {
  DWORD  cbSize;
  DWORD  dwParams;
  DWORD  dwExecutor;
  DWORD  dwSystemType;
  int    nNumSignalBars;
  int    nSignalStrength;
  int    nSNRStrength;
} RILSIGNALQUALITY, RILSIGNALQUALITY;
````

## Members

        
            `cbSize`

            
        
            `dwExecutor`

            
        
            `dwParams`

            
        
            `dwSystemType`

            
        
            `nNumSignalBars`

            
        
            `nSignalStrength`

            
        
            `nSNRStrength`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |