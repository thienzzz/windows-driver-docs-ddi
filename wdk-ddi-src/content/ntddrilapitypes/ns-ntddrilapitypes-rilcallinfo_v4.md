---
UID : NS:ntddrilapitypes.RILCALLINFO_V4
title : RILCALLINFO_V4
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallinfo_v4.htm
old-project : netvista
ms.assetid : 456597d1-e24c-414c-b099-509078cafdc1
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLINFO_V4, *LPRILCALLINFO_V4, RILCALLINFO_V4
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
req.alt-api : RILCALLINFO_V4
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
req.typenames : "*LPRILCALLINFO_V4, RILCALLINFO_V4"
---

# RILCALLINFO_V4 structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILCALLINFO_V4 {
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
  DWORD                           dwFlags;
  RILCALLINFODISCONNECTINITIATOR  dwDisconnectInitiator;
  RILCALLINFODISCONNECTREASON     dwDisconnectReason;
  RILCALLDISCONNECTDETAILS        stDisconnectDetails;
  RILCALLMEDIAOFFERANSWERSET      rcmOfferAnswer;
  RILCALLHANDOVERSTATE            rchsHandoverState;
  RILCALLMODIFICATIONCAUSECODE    dwCallModificationCauseCode;
} RILCALLINFO_V4, RILCALLINFO_V4;
````

## Members

        
            `cbSize`

            
        
            `dwCallModificationCauseCode`

            
        
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

            
        
            `rchsHandoverState`

            
        
            `rcmOfferAnswer`

            
        
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