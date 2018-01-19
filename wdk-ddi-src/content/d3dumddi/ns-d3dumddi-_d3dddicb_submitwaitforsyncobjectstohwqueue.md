---
UID : NS:d3dumddi._D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE
title : _D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE
author : windows-driver-content
description : A structure that holds information to wait for synchronized objects.
old-location : display\d3dddicb_submitwaitforsyncobjectstohwqueue.htm
old-project : display
ms.assetid : 9890EB61-2CED-41AB-9A87-76D5020D84A0
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE, D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dumddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE
req.alt-loc : d3dumddi.h
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
req.typenames : D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE
---

# _D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE structure
A structure that holds information to wait for synchronized objects.

## Syntax
````
typedef struct _D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE {
  HANDLE              hHwQueue;
  UINT                ObjectCount;
  const D3DKMT_HANDLE *ObjectHandleArray;
  const UINT64        *FenceValueArray;
} D3DDDICB_SUBMITWAITFORSYNCOBJECTSTOHWQUEUE;
````

## Members

        
            `FenceValueArray`

            Monitored fence values to be waited on.
        
            `hHwQueue`

            Hardware queue to queue the wait on.
        
            `ObjectCount`

            Number of objects to wait on.
        
            `ObjectHandleArray`

            Handles to monitored fence synchronization objects to wait on.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h |