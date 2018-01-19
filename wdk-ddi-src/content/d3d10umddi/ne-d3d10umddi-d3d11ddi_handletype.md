---
UID : NE:d3d10umddi.D3D11DDI_HANDLETYPE
title : D3D11DDI_HANDLETYPE
author : windows-driver-content
description : Contains values that identify handle types.
old-location : display\d3d11ddi_handletype.htm
old-project : display
ms.assetid : 9ac032fe-b870-49aa-8602-3c7aa997ef9a
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D11DDI_HANDLETYPE, D3D11DDI_HANDLETYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : D3D11DDI_HANDLETYPE is supported beginning with the Windows 7 operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D11DDI_HANDLETYPE
req.alt-loc : d3d10umddi.h
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
req.typenames : D3D11DDI_HANDLETYPE
---

# D3D11DDI_HANDLETYPE Enumeration
Contains values that identify handle types.

## Syntax
````
typedef enum D3D11DDI_HANDLETYPE { 
  D3D10DDI_HT_RESOURCE                           = 0,
  D3D10DDI_HT_SHADERRESOURCEVIEW                 = 1,
  D3D10DDI_HT_RENDERTARGETVIEW                   = 2,
  D3D10DDI_HT_DEPTHSTENCILVIEW                   = 3,
  D3D10DDI_HT_SHADER                             = 4,
  D3D10DDI_HT_ELEMENTLAYOUT                      = 5,
  D3D10DDI_HT_BLENDSTATE                         = 6,
  D3D10DDI_HT_DEPTHSTENCILSTATE                  = 7,
  D3D10DDI_HT_RASTERIZERSTATE                    = 8,
  D3D10DDI_HT_SAMPLERSTATE                       = 9,
  D3D10DDI_HT_QUERY                              = 10,
  D3D11DDI_HT_COMMANDLIST                        = 11,
  D3D11DDI_HT_UNORDEREDACCESSVIEW                = 12,
#if D3D11DDI_MINOR_HEADER_VERSION >= 3
  D3D11_1DDI_HT_DECODE                           = 13,
  D3D11_1DDI_HT_VIDEOPROCESSORENUM               = 14,
  D3D11_1DDI_HT_VIDEOPROCESSOR                   = 15,
  D3D11_1DDI_HT_VIDEODECODEROUTPUTVIEW           = 16,
  D3D11_1DDI_HT_VIDEOPROCESSORINPUTVIEW          = 17,
  D3D11_1DDI_HT_VIDEOPROCESSOROUTPUTVIEW         = 18,
#endif 
#if D3D12DDI_MINOR_HEADER_VERSION >= 2
      D3D12DDI_HT_COMMAND_QUEUE                  = ,
      D3D12DDI_HT_COMMAND_ALLOCATOR              = ,
      D3D12DDI_HT_PIPELINE_STATE                 = ,
      D3D12DDI_HT_COMMAND_LIST                   = ,
      D3D12DDI_HT_FENCE                          = ,
      D3D12DDI_HT_DESCRIPTOR_HEAP                = ,
      D3D12DDI_HT_HEAP                           = ,
      D3D12DDI_HT_UNORDERED_ACCESS_VIEW_COUNTER  = 

#endif } D3D11DDI_HANDLETYPE;
````

## Constants

<table>

<tr>
<td>D3D10DDI_HT_BLENDSTATE</td>
<td>A blend-state handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_DEPTHSTENCILSTATE</td>
<td>A depth-stencil-state handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_DEPTHSTENCILVIEW</td>
<td>A depth-stencil-view handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_ELEMENTLAYOUT</td>
<td>A value that identifies an element-layout handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_QUERY</td>
<td>A query handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_RASTERIZERSTATE</td>
<td>A rasterizer-state handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_RENDERTARGETVIEW</td>
<td>A render-target-view handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_RESOURCE</td>
<td>A resource handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_SAMPLERSTATE</td>
<td>A sampler-state handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_SHADER</td>
<td>A shader handle.</td>
</tr>

<tr>
<td>D3D10DDI_HT_SHADERRESOURCEVIEW</td>
<td>A shader-resource-view handle.</td>
</tr>

<tr>
<td>D3D11_1DDI_HT_DECODE</td>
<td>A video decoder handle.

Supported starting with Windows 8.</td>
</tr>

<tr>
<td>D3D11_1DDI_HT_VIDEODECODEROUTPUTVIEW</td>
<td>A video decoder output-view handle.

Supported starting with Windows 8.</td>
</tr>

<tr>
<td>D3D11_1DDI_HT_VIDEOPROCESSOR</td>
<td>A video processor handle.

Supported starting with Windows 8.</td>
</tr>

<tr>
<td>D3D11_1DDI_HT_VIDEOPROCESSORENUM</td>
<td>A video processor enumeration handle.

Supported starting with Windows 8.</td>
</tr>

<tr>
<td>D3D11_1DDI_HT_VIDEOPROCESSORINPUTVIEW</td>
<td>A video processor input-view handle.

Supported starting with Windows 8.</td>
</tr>

<tr>
<td>D3D11_1DDI_HT_VIDEOPROCESSOROUTPUTVIEW</td>
<td>A video processor output-view handle.

Supported starting with Windows 8.</td>
</tr>

<tr>
<td>D3D11DDI_HT_COMMANDLIST</td>
<td>A command-list handle.</td>
</tr>

<tr>
<td>D3D11DDI_HT_UNORDEREDACCESSVIEW</td>
<td>An unordered-access-view handle.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |