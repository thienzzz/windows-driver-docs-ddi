---
UID : NE:d3dumddi._D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS
title : _D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS
author : windows-driver-content
description : Identifies overlay capabilities.
old-location : display\d3dddi_multiplane_overlay_feature_caps.htm
old-project : display
ms.assetid : 51e44c1c-ca56-4fe3-a27b-d0957df203cf
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS, D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS
req.alt-loc : D3dumddi.h
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
req.typenames : D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS
---

# _D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS Enumeration
Identifies overlay capabilities.

## Syntax
````
typedef enum _D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS { 
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_ROTATION         = 0x1,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_VERTICAL_FLIP    = 0x2,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_HORIZONTAL_FLIP  = 0x4,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_DEINTERLACE      = 0x8,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_RGB              = 0x10,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_YUV              = 0x20,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_BILINEAR_FILTER  = 0x40,
  D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_HIGH_FILTER      = 0x100
} D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS;
````

## Constants

<table>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_BILINEAR_FILTER</td>
<td>The overlay plane supports stretching and shrinking using bilinear filtering.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_DEINTERLACE</td>
<td>Reserved for system use. The user-mode display driver should not use this value.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_HIGH_FILTER</td>
<td>The overlay plane supports stretching and shrinking using filtering that is better than bilinear filtering.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_HORIZONTAL_FLIP</td>
<td>The overlay plane can flip the data horizontally, making it appear as a right-to-left mirror image.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_RGB</td>
<td>The overlay plane supports RGB format.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_ROTATION</td>
<td>The overlay plane can rotate the data 90, 180, and 270 degrees.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_VERTICAL_FLIP</td>
<td>The overlay plane can flip the data vertically, making it appear upside-down.</td>
</tr>

<tr>
<td>D3DDDI_MULTIPLANE_OVERLAY_FEATURE_CAPS_YUV</td>
<td>The overlay plane supports YUV format.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |