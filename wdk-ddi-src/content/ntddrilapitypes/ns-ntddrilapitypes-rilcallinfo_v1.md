---
UID : NS:ntddrilapitypes.RILCALLINFO_V1
title : RILCALLINFO_V1
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallinfo_v1.htm
old-project : netvista
ms.assetid : eae7108f-94d5-4147-b554-189c1a356641
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLINFO_V1, *LPRILCALLINFO_V1, RILCALLINFO_V1
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
req.alt-api : RILCALLINFO_V1
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
req.typenames : "*LPRILCALLINFO_V1, RILCALLINFO_V1"
---

# RILCALLINFO_V1 structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILCALLINFO_V1 {
  DWORD                           cbSize;
  DWORD                           dwParams;
  DWORD                           dwExecutor;
  DWORD                           dwID;
  RILCALLINFODIRECTION            dwDirection;
  RILCALLINFOSTATUS               dwStatus;
  RILCALLTYPE                     dwType;
  RILCALLINFOMULTIPARTY           dwMultiparty;
  RILADDRESS                      raAddress;
  RILSUBADDRESS                   rsaSubAddress;
  WCHAR [256]                     wszDescription;
  RILREMOTEPARTYINFOVALUE         dwNumberPresentationIndicator;
  RILREMOTEPARTYINFOVALUE         dwNamePresentationIndicator;
  BOOL                            fAlienCall;
  RILCALLINFODISCONNECTINITIATOR  dwDisconnectInitiator;
  RILCALLINFODISCONNECTREASON     dwDisconnectReason;
  RILCALLDISCONNECTDETAILS        stDisconnectDetails;
} RILCALLINFO_V1, RILCALLINFO_V1;
````

## Members

        
            `cbSize`

            
        
            `dwDirection`

            
        
            `dwDisconnectInitiator`

            
        
            `dwDisconnectReason`

            
        
            `dwExecutor`

            
        
            `dwID`

            
        
            `dwMultiparty`

            
        
            `dwNamePresentationIndicator`

            
        
            `dwNumberPresentationIndicator`

            
        
            `dwParams`

            
        
            `dwStatus`

            
        
            `dwType`

            
        
            `fAlienCall`

            
        
            `raAddress`

            
        
            `rsaSubAddress`

            
        
            `stDisconnectDetails`

            
        
            `wszDescription`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |