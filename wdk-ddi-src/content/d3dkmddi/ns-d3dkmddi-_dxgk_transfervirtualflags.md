---
UID : NS:d3dkmddi._DXGK_TRANSFERVIRTUALFLAGS
title : _DXGK_TRANSFERVIRTUALFLAGS
author : windows-driver-content
description : DXGK_TRANSFERVIRTUALFLAGS is used as part of an allocation transfer operation.
old-location : display\dxgk_transfervirtualflags.htm
old-project : display
ms.assetid : E5323A30-5BBE-4084-9F99-91FBDD680C12
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_TRANSFERVIRTUALFLAGS, DXGK_TRANSFERVIRTUALFLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_TRANSFERVIRTUALFLAGS
req.alt-loc : d3dkmddi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : DXGK_TRANSFERVIRTUALFLAGS
---

# _DXGK_TRANSFERVIRTUALFLAGS structure
<b>DXGK_TRANSFERVIRTUALFLAGS</b> is used as part of an allocation transfer operation.

## Syntax
````
typedef struct _DXGK_TRANSFERVIRTUALFLAGS {
  union {
    struct {
      UINT Src64KBPages  :1;
      UINT Dst64KBPages  :1;
      UINT Reserved  :30;
    };
    UINT   Flags;
  };
} DXGK_TRANSFERVIRTUALFLAGS;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |