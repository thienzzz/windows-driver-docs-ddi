---
UID : NS:hbapiwmi._SM_SendRNID_OUT
title : _SM_SendRNID_OUT
author : windows-driver-content
description : The SM_SendRNID_OUT structure is used to receive output parameters from the SM_SendRNID method.
old-location : storage\sm_sendrnid_out.htm
old-project : storage
ms.assetid : 177ffc7d-697d-47c5-9692-19cba6734077
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _SM_SendRNID_OUT, *PSM_SendRNID_OUT, SM_SendRNID_OUT
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
req.alt-api : SM_SendRNID_OUT
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
req.typenames : "*PSM_SendRNID_OUT, SM_SendRNID_OUT"
---

# _SM_SendRNID_OUT structure
The SM_SendRNID_OUT structure is used to receive output parameters from the SM_SendRNID method.

## Syntax
````
typedef struct _SM_SendRNID_OUT {
  ULONG HBAStatus;
  ULONG TotalRespBufferSize;
  ULONG OutRespBufferSize;
  UCHAR RespBuffer[1];
} SM_SendRNID_OUT, *PSM_SendRNID_OUT;
````

## Members

        
            `HBAStatus`

            The status of the operation. For a list of allowed values and their descriptions, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a>.
        
            `OutRespBufferSize`

            The size, in bytes, of the data that was actually retrieved.
        
            `RespBuffer`

            The results of the common transport command.
        
            `TotalRespBufferSize`

            The size, in bytes, of the results common transport (CT) command.

    ## Remarks
        The WMI tool suite generates a declaration of the SM_SendRNID_OUT structure in <i>Hbapiwmi.h</i> when it compiles the MS_SM_FabricAndDomainManagementMethod WMI class.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbapiwmi.h (include Hbapiwmi.h) |