---
UID : NS:d3dkmddi._DXGKARG_SETTARGETCONTENTTYPE
title : _DXGKARG_SETTARGETCONTENTTYPE
author : windows-driver-content
description : Used to hold the arguments for DXGKDDI_SETTARGETCONTENTTYPE.
old-location : display\dxgkarg_settargetcontenttype.htm
old-project : display
ms.assetid : BD849954-97CC-4314-B375-22829B0CEE86
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGKARG_SETTARGETCONTENTTYPE, DXGKARG_SETTARGETCONTENTTYPE
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
req.alt-api : DXGKARG_SETTARGETCONTENTTYPE
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
req.typenames : DXGKARG_SETTARGETCONTENTTYPE
---

# _DXGKARG_SETTARGETCONTENTTYPE structure
Used to hold the arguments for <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_settargetcontenttype.md">DXGKDDI_SETTARGETCONTENTTYPE</a>

## Syntax
````
typedef struct _DXGKARG_SETTARGETCONTENTTYPE {
  D3DDDI_VIDEO_PRESENT_TARGET_ID     TargetId;
  D3DKMDT_VIDPN_PRESENT_PATH_CONTENT ContentType;
} DXGKARG_SETTARGETCONTENTTYPE, *PDXGKARG_SETTARGETCONTENTTYPE;
````

## Members

        
            `ContentType`

            A D3DKMDT_VIDPN_PRESENT_PATH_CONTENT value indicating the type of content being presented on the target id for which the driver should optimize.
        
            `TargetId`

            The identifier of a display adapter's video present target.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |