---
UID : NS:hbapiwmi._SM_GetPersistentBinding_IN
title : _SM_GetPersistentBinding_IN
author : windows-driver-content
description : The SM_GetPersistentBinding_IN structure is used to provide input parameters to the SM_GetPersistentBinding method.
old-location : storage\sm_getpersistentbinding_in.htm
old-project : storage
ms.assetid : 6c716394-1e82-40d2-befc-50a0ea88f750
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _SM_GetPersistentBinding_IN, SM_GetPersistentBinding_IN, *PSM_GetPersistentBinding_IN
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
req.alt-api : SM_GetPersistentBinding_IN
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
req.typenames : SM_GetPersistentBinding_IN, *PSM_GetPersistentBinding_IN
---

# _SM_GetPersistentBinding_IN structure
The SM_GetPersistentBinding_IN structure is used to provide input parameters to the SM_GetPersistentBinding method.

## Syntax
````
typedef struct _SM_GetPersistentBinding_IN {
  UCHAR HbaPortWWN[8];
  UCHAR DomainPortWWN[8];
  ULONG InEntryCount;
} SM_GetPersistentBinding_IN, *PSM_GetPersistentBinding_IN;
````

## Members

        
            `DomainPortWWN`

            A worldwide name (WWN) that specifies the SAS domain worldwide name of the local port.
        
            `HbaPortWWN`

            The worldwide name (WWN) of the local port whose events the WMI client will receive.
        
            `InEntryCount`

            The number of persistent bindings that are associated with the HBA.

    ## Remarks
        The WMI tool suite generates a declaration of the SM_GetPersistentBinding_IN structure in <i>Hbapiwmi.h</i> when it compiles the MS_SM_TargetInformationMethods WMI class.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbapiwmi.h (include Hbapiwmi.h) |