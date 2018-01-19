---
UID : NS:rilapitypes.RILCALLDISCONNECTDETAILS
title : RILCALLDISCONNECTDETAILS
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcalldisconnectdetails_2.htm
old-project : netvista
ms.assetid : 57b4d120-e12a-4821-a379-a392b804590c
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLDISCONNECTDETAILS, *LPRILCALLDISCONNECTDETAILS, RILCALLDISCONNECTDETAILS
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
req.alt-api : RILCALLDISCONNECTDETAILS
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
req.typenames : "*LPRILCALLDISCONNECTDETAILS, RILCALLDISCONNECTDETAILS"
req.product : Windows 10 or later.
---

# RILCALLDISCONNECTDETAILS structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILCALLDISCONNECTDETAILS {
  RILCALLDISCONNECTDETAILSDISCONNECTGROUP  dwDisconnectGroup;
  NULL                                     RILCAUSEUNION;
  RILCAUSEUNION                            causeUnion;
  NULL                                     switch_is;
  NULL                                     dwDisconnectGroup;
  RILGPPCAUSE                              unGPPCause;
  NULL                                     case;
  NULL                                     RIL_CD_3GPP_NETWORK_CAUSE;
  RILGPPREJECTCAUSE                        unGPPRejectCause;
  NULL                                     case;
  NULL                                     RIL_CD_3GPP_REJECT_CAUSE;
  RILGPP2CAUSE                             unGPP2Cause;
  NULL                                     case;
  NULL                                     RIL_CD_3GPP2_VENDOR_CAUSE;
  RILIMSSIPCAUSE                           unIMSSIPCause;
  NULL                                     case;
  NULL                                     RIL_CD_IMS_SIP_CAUSE;
  RILCALLDISCONNECTDETAILSASCODE           dwASCode;
  NULL                                     case;
  NULL                                     RIL_CD_AS_CAUSE;
  DWORD                                    dwOtherCode;
  NULL                                     case;
  NULL                                     RIL_CD_OTHER_CAUSE;
} RILCALLDISCONNECTDETAILS, RILCALLDISCONNECTDETAILS;
````

## Members

        
            `causeUnion`

            
        
            `dwDisconnectGroup`

            
        
            `RILCAUSEUNION`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapitypes.h |