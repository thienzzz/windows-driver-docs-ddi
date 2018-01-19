---
UID : NS:d3dkmddi.DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO
title : DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO
author : windows-driver-content
description : Specifies limitations on hardware support of multiplane overlays.
old-location : display\dxgk_check_multiplane_overlay_support_return_info.htm
old-project : display
ms.assetid : EA440D77-18E6-4EB4-8621-50C3233DFEA6
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO, DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO
req.alt-loc : D3dkmddi.h
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
req.typenames : DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO
---

# DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO structure
Specifies limitations on hardware support of multiplane overlays.

## Syntax
````
typedef struct DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO {
  union {
    struct {
      UINT FailingPlane;
      UINT TryAgain;
      UINT Reserved  :27;
    };
    UINT Value;
  };
} DXGK_CHECK_MULTIPLANE_OVERLAY_SUPPORT_RETURN_INFO;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |