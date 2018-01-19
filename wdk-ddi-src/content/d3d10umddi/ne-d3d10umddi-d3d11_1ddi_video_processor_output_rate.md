---
UID : NE:d3d10umddi.D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE
title : D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE
author : windows-driver-content
description : Specifies the rate at which the video processor produces output frames from an input stream.
old-location : display\d3d11_1ddi_video_processor_output_rate.htm
old-project : display
ms.assetid : ff34c208-9b42-4f72-bb2a-43f3bb44fd68
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE, D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE
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
req.alt-api : D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE
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
req.typenames : D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE
---

# D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE Enumeration
Specifies the rate at which the video processor produces output frames from an input stream.

## Syntax
````
typedef enum D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE { 
  D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE_NORMAL  = 0,
  D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE_HALF    = 1,
  D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE_CUSTOM  = 2
} D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE;
````

## Constants

<table>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE_CUSTOM</td>
<td>The output is a custom frame rate.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE_HALF</td>
<td>The output is half the frame rate.</td>
</tr>

<tr>
<td>D3D11_1DDI_VIDEO_PROCESSOR_OUTPUT_RATE_NORMAL</td>
<td>The output is the normal frame rate.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |