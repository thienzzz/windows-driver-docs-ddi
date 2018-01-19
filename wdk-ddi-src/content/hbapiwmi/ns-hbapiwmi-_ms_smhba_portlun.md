---
UID : NS:hbapiwmi._MS_SMHBA_PORTLUN
title : _MS_SMHBA_PORTLUN
author : windows-driver-content
description : The MS_SMHBA_PORTLUN structure reports target LUN information that is associated with a port.
old-location : storage\ms_smhba_portlun.htm
old-project : storage
ms.assetid : cf62685f-7b4d-4671-a755-d59a593bf5d6
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _MS_SMHBA_PORTLUN, MS_SMHBA_PORTLUN, *PMS_SMHBA_PORTLUN
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
req.alt-api : MS_SMHBA_PORTLUN
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
req.typenames : MS_SMHBA_PORTLUN, *PMS_SMHBA_PORTLUN
---

# _MS_SMHBA_PORTLUN structure
The MS_SMHBA_PORTLUN structure reports target LUN information that is associated with a port.

## Syntax
````
typedef struct _MS_SMHBA_PORTLUN {
  UCHAR     PortWWN[8];
  UCHAR     domainPortWWN[8];
  ULONGLONG TargetLun;
} MS_SMHBA_PORTLUN, *PMS_SMHBA_PORTLUN;
````

## Members

        
            `domainPortWWN`

            A worldwide name that specifies the SAS domain worldwide name of the local port.
        
            `PortWWN`

            The worldwide name of the local port whose events the WMI client will receive.
        
            `TargetLun`

            The target LUN number.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbapiwmi.h (include Hbapiwmi.h) |