---
UID : NS:d3dkmddi._DXGK_MULTIPLANE_OVERLAY_PLANE3
title : _DXGK_MULTIPLANE_OVERLAY_PLANE3
author : windows-driver-content
description : Specifies an overlay plane to display in a call to the DxgkDdiSetVidPnSourceAddressWithMultiPlaneOverlay3 function.
old-location : display\dxgk_multiplane_overlay_plane3.htm
old-project : display
ms.assetid : 2C524702-A819-4B91-B236-E00B2820813C
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_MULTIPLANE_OVERLAY_PLANE3, DXGK_MULTIPLANE_OVERLAY_PLANE3
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
req.alt-api : DXGK_MULTIPLANE_OVERLAY_PLANE3
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
req.typenames : DXGK_MULTIPLANE_OVERLAY_PLANE3
---

# _DXGK_MULTIPLANE_OVERLAY_PLANE3 structure
Specifies an overlay plane to display in a call to the DxgkDdiSetVidPnSourceAddressWithMultiPlaneOverlay3 function.

## Syntax
````
typedef struct _DXGK_MULTIPLANE_OVERLAY_PLANE3 {
  UINT                                 LayerIndex;
  ULONGLONG                            PresentId;
  DXGK_PLANE_SPECIFIC_INPUT_FLAGS      InputFlags;
  DXGK_PLANE_SPECIFIC_OUTPUT_FLAGS     OutputFlags;
  UINT                                 MaxImmediateFlipLine;
  UINT                                 ContextCount;
  HANDLE                               *pContext;
  DXGK_PRIMARYDATA                     *pPrimaryData;
  UINT                                 DriverPrivateDataSize;
  PVOID                                pDriverPrivateData;
  DXGK_MULTIPLANE_OVERLAY_ATTRIBUTES3  PlaneAttributes;
} DXGK_MULTIPLANE_OVERLAY_PLANE3;
````

## Members

        
            `ContextCount`

            The number of contexts in the array that the Context member specifies.
        
            `DriverPrivateDataSize`

            The size of the private driver data.
        
            `InputFlags`

            A DXGK_PLANE_SPECIFIC_INPUT_FLAGS structure that identifies any plane specific display operations to perform.
        
            `LayerIndex`

            The zero-based index of the overlay plane to display. The top plane (in the z-direction) has index zero. The planes' index values must be sequential from top to bottom.
        
            `MaxImmediateFlipLine`

            The display line delineating whether a VSYNC flip should be promoted to an immediate flip, where line 0 corresponds to the first active pixel of the frame. This value is ignored for non-VSYNC flips.



This value is -1 when promotion from a VSYNC flip to an immediate flip is not desired. In this case, the flip will always wait for the next VSYNC.

For a value other than -1, the driver should promote this flip to an immediate flip if the HW has not yet started reading from the specified display line. Values of 0 can be promoted to immediate flips if the HW has latched registers for the current display frame but has not yet started scanning the first active pixel.



The display line value is relative to the physical mode that is set. If the display is performing scaling, display line is relative to the size after scaling has been applied.





When a VSYNC flip is promoted to an immediate flip, the driver should set DXGK_PLANE_SPECIFIC_OUTPUT_FLAGS. FlipConvertedToImmediate to TRUE.
        
            `OutputFlags`

            A DXGK_PLANE_SPECIFIC_OUTPUT_FLAGS structure containing status returned by the driver.
        
            `pDriverPrivateData`

            Private driver data.
        
            `PlaneAttributes`

            A structure of type DXGK_MULTIPLANE_OVERLAY_ATTRIBUTES3 that specifies overlay plane attributes.
        
            `PresentId`

            A 64 bit per-plane identifier used by the driver to report completion of the overlay command.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |