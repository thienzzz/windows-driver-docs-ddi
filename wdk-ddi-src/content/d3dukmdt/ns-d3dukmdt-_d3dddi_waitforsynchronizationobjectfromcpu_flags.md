---
UID : NS:d3dukmdt._D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS
title : _D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS
author : windows-driver-content
description : D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS describes the type of input synchronization objects to wait for.
old-location : display\d3dddi_waitforsynchronizationobjectfromcpu_flags.htm
old-project : display
ms.assetid : 2283D20F-D256-48E5-BFD2-D3ACACD7BF1C
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS, D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dukmdt.h
req.include-header : D3dumddi.h, D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS
req.alt-loc : d3dukmdt.h
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
req.typenames : D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS
---

# _D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS structure
<b>D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS</b> describes the type of input synchronization objects to wait for.

## Syntax
````
typedef struct _D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS {
  union {
    struct {
      UINT WaitAny  :1;
      UINT Reserved  :31;
    };
    UINT Value;
  };
} D3DDDI_WAITFORSYNCHRONIZATIONOBJECTFROMCPU_FLAGS;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dukmdt.h (include D3dumddi.h, D3dkmddi.h) |