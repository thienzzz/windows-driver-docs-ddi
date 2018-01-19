---
UID : NS:rilapitypes.RILCALLINFO_V2
title : RILCALLINFO_V2
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallinfo_v2_2.htm
old-project : netvista
ms.assetid : bf7d8586-21da-4f62-b9e6-4ffe7ca546e1
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLINFO_V2, *LPRILCALLINFO_V2, RILCALLINFO_V2
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
req.alt-api : RILCALLINFO_V2
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
req.typenames : "*LPRILCALLINFO_V2, RILCALLINFO_V2"
req.product : Windows 10 or later.
---

# RILCALLINFO_V2 structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILCALLINFO_V2 {
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
  WCHAR [MAXLENGTH_DESCRIPTION]   wszDescription;
  RILREMOTEPARTYINFOVALUE         dwNumberPresentationIndicator;
  RILREMOTEPARTYINFOVALUE         dwNamePresentationIndicator;
  DWORD                           dwFlags;
  RILCALLINFODISCONNECTINITIATOR  dwDisconnectInitiator;
  RILCALLINFODISCONNECTREASON     dwDisconnectReason;
  RILCALLDISCONNECTDETAILS        stDisconnectDetails;
} RILCALLINFO_V2, RILCALLINFO_V2;
````

## Members

        
            `cbSize`

            
        
            `dwDirection`

            
        
            `dwDisconnectInitiator`

            
        
            `dwDisconnectReason`

            
        
            `dwExecutor`

            
        
            `dwFlags`

            
        
            `dwID`

            
        
            `dwMultiparty`

            
        
            `dwNamePresentationIndicator`

            
        
            `dwNumberPresentationIndicator`

            
        
            `dwParams`

            
        
            `dwStatus`

            
        
            `dwType`

            
        
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
| **Header** | rilapitypes.h |