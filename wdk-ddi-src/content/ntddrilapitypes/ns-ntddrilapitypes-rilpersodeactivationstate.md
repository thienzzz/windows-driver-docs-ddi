---
UID : NS:ntddrilapitypes.RILPERSODEACTIVATIONSTATE
title : RILPERSODEACTIVATIONSTATE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilpersodeactivationstate.htm
old-project : netvista
ms.assetid : a43948e4-ab31-495a-ace2-4cb4a1119af5
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILPERSODEACTIVATIONSTATE, RILPERSODEACTIVATIONSTATE, *LPRILPERSODEACTIVATIONSTATE
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
req.alt-api : RILPERSODEACTIVATIONSTATE
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
req.typenames : RILPERSODEACTIVATIONSTATE, *LPRILPERSODEACTIVATIONSTATE
---

# RILPERSODEACTIVATIONSTATE structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILPERSODEACTIVATIONSTATE {
  DWORD                                  cbSize;
  DWORD                                  dwParams;
  RILPERSODEACTIVATIONSTATEDEPERSOSTATE  dwDePersoState;
  DWORD                                  dwNumCKAttemptsLeft;
  DWORD                                  dwNumPUKAttemptsLeft;
} RILPERSODEACTIVATIONSTATE, RILPERSODEACTIVATIONSTATE;
````

## Members

        
            `cbSize`

            
        
            `dwDePersoState`

            
        
            `dwNumCKAttemptsLeft`

            
        
            `dwNumPUKAttemptsLeft`

            
        
            `dwParams`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |