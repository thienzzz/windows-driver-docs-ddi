---
UID : NE:d3d10umddi.D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS
title : D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS
author : windows-driver-content
description : Specifies the automatic image processing capabilities of the video processor.
old-location : display\d3d11_1ddi_video_processor_auto_stream_caps.htm
old-project : display
ms.assetid : 00334dec-b84a-49d4-bd09-440eb7a1b79d
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS, D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS
req.alt-loc : D3d10umddi.h
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
req.typenames : D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS
---

# D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS Enumeration
Specifies the automatic image processing capabilities of the video processor.

## Syntax
````
typedef enum D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS { 
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_DENOISE              = 0x01,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_DERINGING            = 0x02,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_EDGE_ENHANCEMENT     = 0x04,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_COLOR_CORRECTION     = 0x08,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_FLESH_TONE_MAPPING   = 0x10,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_IMAGE_STABILIZATION  = 0x20,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_SUPER_RESOLUTION     = 0x40,
  D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_ANAMORPHIC_SCALING   = 0x80
} D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS;
````

## Constants

<table>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_ANAMORPHIC_SCALING</td>
<td>Anamorphic scaling.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_COLOR_CORRECTION</td>
<td>Color correction.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_DENOISE</td>
<td>Denoise.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_DERINGING</td>
<td>Deringing.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_EDGE_ENHANCEMENT</td>
<td>Edge enhancement.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_FLESH_TONE_MAPPING</td>
<td>Flesh-tone mapping.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_IMAGE_STABILIZATION</td>
<td>Image stabilization.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_AUTO_STREAM_CAPS_SUPER_RESOLUTION</td>
<td>Enhanced image resolution.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |