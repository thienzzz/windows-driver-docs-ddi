---
UID : NS:ntddrilapitypes.RILSETCALLFORWARDINGSTATUSPARAMS
title : RILSETCALLFORWARDINGSTATUSPARAMS
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilsetcallforwardingstatusparams.htm
old-project : netvista
ms.assetid : 7863a72d-e3cc-4627-a956-7e5a080c4aad
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILSETCALLFORWARDINGSTATUSPARAMS, RILSETCALLFORWARDINGSTATUSPARAMS, *LPRILSETCALLFORWARDINGSTATUSPARAMS
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
req.alt-api : RILSETCALLFORWARDINGSTATUSPARAMS
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
req.typenames : RILSETCALLFORWARDINGSTATUSPARAMS, *LPRILSETCALLFORWARDINGSTATUSPARAMS
---

# RILSETCALLFORWARDINGSTATUSPARAMS structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILSETCALLFORWARDINGSTATUSPARAMS {
  DWORD                            dwExecutor;
  RILCALLFORWARDINGSETTINGSREASON  dwReason;
  BOOL                             fAllClasses;
  DWORD                            dwInfoClasses;
  RILSERVICESETTINGSSTATUS         dwStatus;
} RILSETCALLFORWARDINGSTATUSPARAMS, RILSETCALLFORWARDINGSTATUSPARAMS;
````

## Members

        
            `dwExecutor`

            
        
            `dwInfoClasses`

            
        
            `dwReason`

            
        
            `dwStatus`

            
        
            `fAllClasses`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |