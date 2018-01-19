---
UID : NS:d3d12umddi.D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020
title : D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020
author : windows-driver-content
description : This structure contains device functions for core features in video.
old-location : display\d3d12ddi_device_funcs_core_video_0020.htm
old-project : display
ms.assetid : E880F758-A872-4B59-BF7D-602C3ACDA490
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020, D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3d12umddi.h
req.include-header : D3d12umddi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020
req.alt-loc : D3d12umddi.h
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
req.typenames : D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020
---

# D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020 structure
This structure contains device functions for core features in  video.

## Syntax
````
typedef struct _D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020 {
  PFND3D12DDI_GETPAGEABLESIZE_0020 pfnGetPageableSize;
} D3D12DDI_DEVICE_FUNCS_CORE_VIDEO_0020;
````

## Members

        
            `pfnGetPageableSize`

            A pointer for a callback function to get pageable size.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |