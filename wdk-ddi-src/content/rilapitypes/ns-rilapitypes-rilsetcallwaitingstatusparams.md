---
UID : NS:rilapitypes.RILSETCALLWAITINGSTATUSPARAMS
title : RILSETCALLWAITINGSTATUSPARAMS
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilsetcallwaitingstatusparams_2.htm
old-project : netvista
ms.assetid : d6b68e8c-aae1-4a50-8cb3-514379029982
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILSETCALLWAITINGSTATUSPARAMS, RILSETCALLWAITINGSTATUSPARAMS, *LPRILSETCALLWAITINGSTATUSPARAMS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : rilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILSETCALLWAITINGSTATUSPARAMS
req.alt-loc : rilapitypes.h
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
req.typenames : RILSETCALLWAITINGSTATUSPARAMS, *LPRILSETCALLWAITINGSTATUSPARAMS
req.product : Windows 10 or later.
---

# RILSETCALLWAITINGSTATUSPARAMS structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILSETCALLWAITINGSTATUSPARAMS {
  DWORD                     dwExecutor;
  BOOL                      fAllClasses;
  DWORD                     dwInfoClasses;
  RILSERVICESETTINGSSTATUS  dwStatus;
} RILSETCALLWAITINGSTATUSPARAMS, RILSETCALLWAITINGSTATUSPARAMS;
````

## Members

        
            `dwExecutor`

            
        
            `dwInfoClasses`

            
        
            `dwStatus`

            
        
            `fAllClasses`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapitypes.h |