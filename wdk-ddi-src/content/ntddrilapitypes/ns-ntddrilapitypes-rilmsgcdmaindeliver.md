---
UID : NS:ntddrilapitypes.RILMSGCDMAINDELIVER
title : RILMSGCDMAINDELIVER
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmsgcdmaindeliver.htm
old-project : netvista
ms.assetid : fdff17ac-2ffd-45b0-8f01-a21af1ffa9d0
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMSGCDMAINDELIVER, RILMSGCDMAINDELIVER, *LPRILMSGCDMAINDELIVER
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
req.alt-api : RILMSGCDMAINDELIVER
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
req.typenames : RILMSGCDMAINDELIVER, *LPRILMSGCDMAINDELIVER
---

# RILMSGCDMAINDELIVER structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILMSGCDMAINDELIVER {
  RILADDRESS                raOrigAddress;
  RILSUBADDRESS             rsaOrigSubaddr;
  RILSYSTEMTIME             stSCReceiveTime;
  RILSYSTEMTIME             stValidityPeriodAbs;
  RILSYSTEMTIME             stValidityPeriodRel;
  RILSYSTEMTIME             stDeferredDelTimeAbs;
  RILSYSTEMTIME             stDeferredDelTimeRel;
  DWORD                     dwNumMsgs;
  RILADDRESS                raCallBackNumber;
  RILMSGCDMAMSGPRIORITY     dwMsgPriority;
  DWORD                     dwAlertOnMsgDelivery;
  RILMSGCDMAMSGPRIVACY      dwMsgPrivacy;
  BOOL                      bUserAckRequest;
  RILMSGCDMAMSGDISPLAYMODE  dwMsgDisplayMode;
  DWORD                     dwTeleservice;
  DWORD                     dwServiceID;
  DWORD                     dwMsgID;
  RILMSGCDMALANGUAGE        dwMsgLang;
  RILMSGCDMAMSGENCODING     dwMsgEncoding;
  DWORD                     cbHdrLength;
  DWORD                     cchMsgLength;
  BYTE [140]                rgbHdr;
  BYTE [256]                rgbMsg;
} RILMSGCDMAINDELIVER, RILMSGCDMAINDELIVER;
````

## Members

        
            `bUserAckRequest`

            
        
            `cbHdrLength`

            
        
            `cchMsgLength`

            
        
            `dwAlertOnMsgDelivery`

            
        
            `dwMsgDisplayMode`

            
        
            `dwMsgEncoding`

            
        
            `dwMsgID`

            
        
            `dwMsgLang`

            
        
            `dwMsgPriority`

            
        
            `dwMsgPrivacy`

            
        
            `dwNumMsgs`

            
        
            `dwServiceID`

            
        
            `dwTeleservice`

            
        
            `raCallBackNumber`

            
        
            `raOrigAddress`

            
        
            `rgbHdr`

            
        
            `rgbMsg`

            
        
            `rsaOrigSubaddr`

            
        
            `stDeferredDelTimeAbs`

            
        
            `stDeferredDelTimeRel`

            
        
            `stSCReceiveTime`

            
        
            `stValidityPeriodAbs`

            
        
            `stValidityPeriodRel`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |