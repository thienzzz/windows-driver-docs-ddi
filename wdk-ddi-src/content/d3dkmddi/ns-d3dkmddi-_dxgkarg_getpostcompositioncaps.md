---
UID : NS:d3dkmddi._DXGKARG_GETPOSTCOMPOSITIONCAPS
title : _DXGKARG_GETPOSTCOMPOSITIONCAPS
author : windows-driver-content
description : Arguments for the DxgkDdiGetPostCompositionCaps function.
old-location : display\dxgkarg_getpostcompositioncaps.htm
old-project : display
ms.assetid : 0C8A0F83-9D12-46F1-A8B1-3BCF219A3BF7
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGKARG_GETPOSTCOMPOSITIONCAPS, DXGKARG_GETPOSTCOMPOSITIONCAPS, *IN_OUT_PDXGKARG_GETPOSTCOMPOSITIONCAPS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGKARG_GETPOSTCOMPOSITIONCAPS
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
req.typenames : DXGKARG_GETPOSTCOMPOSITIONCAPS
---

# _DXGKARG_GETPOSTCOMPOSITIONCAPS structure
Arguments for the DxgkDdiGetPostCompositionCaps function.

## Syntax
````
typedef struct _DXGKARG_GETPOSTCOMPOSITIONCAPS {
  D3DDDI_VIDEO_PRESENT_SOURCE_ID VidPnSourceId;
  float                          MaxStretchFactor;
  float                          MaxShrinkFactor;
} DXGKARG_GETPOSTCOMPOSITIONCAPS;
````

## Members

        
            `MaxShrinkFactor`

            [out] Indicates the maximum shrink factor that can be applied.
        
            `MaxStretchFactor`

            [out] Indicates the maximum stretch factor that can be applied.
        
            `VidPnSourceId`

            [in] Indicates the VidPn source for which post composition capabilities are queried.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |