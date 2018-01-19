---
UID : NS:ntddrilapitypes.RILDRVNOTIFICATION
title : RILDRVNOTIFICATION
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rildrvnotification.htm
old-project : netvista
ms.assetid : 15567aae-a8ab-4289-9dd7-5bf7df80bfc9
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILDRVNOTIFICATION, *LPRILDRVNOTIFICATION, RILDRVNOTIFICATION
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
req.alt-api : RILDRVNOTIFICATION
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
req.typenames : "*LPRILDRVNOTIFICATION, RILDRVNOTIFICATION"
---

# RILDRVNOTIFICATION structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILDRVNOTIFICATION {
  DWORD    cbSize;
  DWORD    cbSizeNeeded;
  DWORD    dwCode;
  HRESULT  hrCmdID;
  DWORD    dwDataSize;
  BYTE [1] pbData;
} RILDRVNOTIFICATION, RILDRVNOTIFICATION;
````

## Members

        
            `cbSize`

            
        
            `cbSizeNeeded`

            
        
            `dwCode`

            
        
            `dwDataSize`

            
        
            `hrCmdID`

            
        
            `pbData`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |