---
UID : NS:hbapiwmi._SM_SendTEST_IN
title : _SM_SendTEST_IN
author : windows-driver-content
description : The SM_SendTEST_IN structure is used to provide input parameters to the SM_SendTEST method.
old-location : storage\sm_sendtest_in.htm
old-project : storage
ms.assetid : 5bb0620e-b271-4af6-b528-b904910b8a6c
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _SM_SendTEST_IN, SM_SendTEST_IN, *PSM_SendTEST_IN
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : hbapiwmi.h
req.include-header : Hbapiwmi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : SM_SendTEST_IN
req.alt-loc : hbapiwmi.h
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
req.typenames : SM_SendTEST_IN, *PSM_SendTEST_IN
---

# _SM_SendTEST_IN structure
The SM_SendTEST_IN structure is used to provide input parameters to the SM_SendTEST method.

## Syntax
````
typedef struct _SM_SendTEST_IN {
  UCHAR HbaPortWWN[8];
  UCHAR DestWWN[8];
  ULONG DestFCID;
  ULONG ReqBufferSize;
  UCHAR ReqBuffer[1];
} SM_SendTEST_IN, *PSM_SendTEST_IN;
````

## Members

        
            `DestFCID`

            The address identifier of the remote port.
        
            `DestWWN`

            The remote HBA port worldwide name (WWN) to which the command will be sent.
        
            `HbaPortWWN`

            The local HBA port worldwide name (WWN).
        
            `ReqBuffer`

            The request buffer data.
        
            `ReqBufferSize`

            The request buffer size.

    ## Remarks
        The WMI tool suite generates a declaration of the SM_SendTEST_IN structure in <i>Hbapiwmi.h</i> when it compiles the MS_SM_FabricAndDomainManagementMethod WMI class.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbapiwmi.h (include Hbapiwmi.h) |