---
UID : NS:igpupvdev._LUID
title : _LUID
author : windows-driver-content
description : The locally unique identifier (LUID) is a 64-bit value guaranteed to be unique only on the system on which it was generated.
old-location : netvista\luid.htm
old-project : netvista
ms.assetid : 9547d3e1-a811-4b89-be71-f7cf81e92b93
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _LUID, LUID, *PLUID
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : igpupvdev.h
req.include-header : Fwptypes.h, Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : LUID
req.alt-loc : igpupvdev.h
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
req.typenames : LUID
---

# _LUID structure
The locally unique identifier (LUID) is a 64-bit value guaranteed to be unique only on the system on
  which it was generated. The uniqueness of an LUID is guaranteed only until the system is restarted. 
  

An LUID is not for direct manipulation. Drivers must use support routines and structures to manipulate
  LUID values.

## Syntax
````
typedef struct _LUID {
  DWORD LowPart;
  LONG  HighPart;
} LUID, *PLUID;
````

## Members

        
            `HighPart`

            High order bits.
        
            `LowPart`

            Low order bits.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | igpupvdev.h (include Fwptypes.h, Fwpsk.h) |