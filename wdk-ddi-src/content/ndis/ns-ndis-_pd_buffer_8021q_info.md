---
UID : NS:ndis._PD_BUFFER_8021Q_INFO
title : _PD_BUFFER_8021Q_INFO
author : windows-driver-content
description : This structure contains the IEEE 802.1Q information.
old-location : netvista\pd_buffer_8021q_info.htm
old-project : netvista
ms.assetid : B5B2051E-C62F-4E3D-9C52-DE46145A2C24
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _PD_BUFFER_8021Q_INFO, PD_BUFFER_8021Q_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ndis.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PD_BUFFER_8021Q_INFO
req.alt-loc : Ndis.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : See Remarks section
req.typenames : PD_BUFFER_8021Q_INFO
---

# _PD_BUFFER_8021Q_INFO structure
This structure contains the IEEE 802.1Q information.

## Syntax
````
typedef struct _PD_BUFFER_8021Q_INFO {
  UINT16 UserPriority  :3;
  UINT16 CanonicalFormatId  :1;
  UINT16 VlanId  :12;
} PD_BUFFER_8021Q_INFO, *PPD_BUFFER_8021Q_INFO;
````

## Members

        
            `CanonicalFormatId`

            The canonical format ID.
        
            `UserPriority`

            The user priority.
        
            `VlanId`

            The virtual LAN ID.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h |