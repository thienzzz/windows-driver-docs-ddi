---
UID : NS:hbapiwmi._SM_GetLUNStatistics_OUT
title : _SM_GetLUNStatistics_OUT
author : windows-driver-content
description : The SM_GetLUNStatistics_OUT structure is used to receive output parameters from the SM_GetLUNStatistics_OUT method.
old-location : storage\sm_getlunstatistics_out.htm
old-project : storage
ms.assetid : 5b7e4eb2-d6e9-49c9-b84f-72dd4198c0ce
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _SM_GetLUNStatistics_OUT, *PSM_GetLUNStatistics_OUT, SM_GetLUNStatistics_OUT
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
req.alt-api : SM_GetLUNStatistics_OUT
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
req.typenames : "*PSM_GetLUNStatistics_OUT, SM_GetLUNStatistics_OUT"
---

# _SM_GetLUNStatistics_OUT structure
The SM_GetLUNStatistics_OUT structure is used to receive output parameters from the SM_GetLUNStatistics_OUT method.

## Syntax
````
typedef struct _SM_GetLUNStatistics_OUT {
  ULONG                       HBAStatus;
  MS_SMHBA_PROTOCOLSTATISTICS ProtocolStatistics;
} SM_GetLUNStatistics_OUT, *PSM_GetLUNStatistics_OUT;
````

## Members

        
            `HBAStatus`

            The status of the operation. For a list of allowed values and their descriptions, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a>.
        
            `ProtocolStatistics`

            A structure of type <a href="..\hbapiwmi\ns-hbapiwmi-_ms_smhba_protocolstatistics.md">MS_SMHBA_PROTOCOLSTATISTICS</a> that is used to report protocol traffic statistics on a port.

    ## Remarks
        The WMI tool suite generates a declaration of the SM_GetLUNStatistics_OUT structure in <i>Hbapiwmi.h</i> when it compiles the MS_SM_TargetInformationMethods WMI class.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbapiwmi.h (include Hbapiwmi.h) |