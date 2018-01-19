---
UID : NS:ntddrilapitypes.RILMSGINSTATUS
title : RILMSGINSTATUS
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmsginstatus.htm
old-project : netvista
ms.assetid : 383ed544-c8c8-42a0-a7de-57f0f4072611
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMSGINSTATUS, *LPRILMSGINSTATUS, RILMSGINSTATUS
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
req.alt-api : RILMSGINSTATUS
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
req.typenames : "*LPRILMSGINSTATUS, RILMSGINSTATUS"
---

# RILMSGINSTATUS structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILMSGINSTATUS {
  DWORD                       dwMsgID;
  RILADDRESS                  raTgtRecipAddress;
  RILSYSTEMTIME               stTgtSCReceiveTime;
  RILSYSTEMTIME               stTgtDischargeTime;
  DWORD                       dwReserved;
  RILMSGINSTATUSTGTDLVSTATUS  dwTgtDlvStatus;
  RILMSGPROTOCOLID            dwProtocolID;
  RILMSGDCS                   rmdDataCoding;
  DWORD                       cbHdrLength;
  DWORD                       cchMsgLength;
  BYTE [256]                  rgbHdr;
  BYTE [512]                  rgbMsg;
} RILMSGINSTATUS, RILMSGINSTATUS;
````

## Members

        
            `cbHdrLength`

            
        
            `cchMsgLength`

            
        
            `dwMsgID`

            
        
            `dwProtocolID`

            
        
            `dwReserved`

            
        
            `dwTgtDlvStatus`

            
        
            `raTgtRecipAddress`

            
        
            `rgbHdr`

            
        
            `rgbMsg`

            
        
            `rmdDataCoding`

            
        
            `stTgtDischargeTime`

            
        
            `stTgtSCReceiveTime`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |