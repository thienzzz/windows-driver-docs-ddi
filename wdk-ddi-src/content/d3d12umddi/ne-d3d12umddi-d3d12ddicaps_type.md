---
UID : NE:d3d12umddi.D3D12DDICAPS_TYPE
title : D3D12DDICAPS_TYPE
author : windows-driver-content
description : Specifies a capability type.
old-location : display\d3d12ddicaps_type.htm
old-project : display
ms.assetid : C74697BF-A191-4371-9F23-7F655EBC53B3
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDICAPS_TYPE, D3D12DDICAPS_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d12umddi.h
req.include-header : D3d12umddi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D12DDICAPS_TYPE
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
req.typenames : D3D12DDICAPS_TYPE
---

# D3D12DDICAPS_TYPE Enumeration
Specifies a capability type.

## Syntax
````
typedef enum D3D12DDICAPS_TYPE { 
  D3D12DDICAPS_TYPE_TEXTURE_LAYOUT                         = 1000,
  D3D12DDICAPS_TYPE_SWIZZLE_PATTERN                        = 1001,
  D3D12DDICAPS_TYPE_MEMORY_ARCHITECTURE                    = 1002,
  D3D12DDICAPS_TYPE_TEXTURE_LAYOUT_SETS                    = 1003,
  D3D12DDICAPS_TYPE_SHADER                                 = 1004,
  D3D12DDICAPS_TYPE_ARCHITECTURE_INFO                      = 1005,
  D3D12DDICAPS_TYPE_D3D12_OPTIONS                          = 1006,
  D3D12DDICAPS_TYPE_3DPIPELINESUPPORT                      = 1007,
  D3D12DDICAPS_TYPE_JPEG_OPTIONS                           = 1008,
  D3D12DDICAPS_TYPE_GPUVA_CAPS                             = 1009,
  D3D12DDICAPS_TYPE_TEXTURE_LAYOUT1                        = 1010,
  D3D12DDICAPS_TYPE_0011_SHADER_MODELS                     = 1012,
  D3D12DDICAPS_TYPE_0020_CONTENT_PROTECTION_SUPPORT        = 1057,
  D3D12DDICAPS_TYPE_0020_CONTENT_PROTECTION_DRM_SUPPORT    = 1058,
  D3D12DDICAPS_TYPE_0022_CPU_PAGE_TABLE_FALSE_POSITIVES    = 1059,
  D3D12DDICAPS_TYPE_0022_TEXTURE_LAYOUT                    = 1060,
  D3D12DDICAPS_TYPE_0022_SWIZZLE_PATTERN                   = 1061,
  D3D12DDICAPS_TYPE_0023_UMD_BASED_COMMAND_QUEUE_PRIORITY  = 1062
} D3D12DDICAPS_TYPE;
````

## Constants

<table>

<tr>
<td>D3D12DDICAPS_TYPE_0011_SHADER_MODELS</td>
<td>Shader models.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_0022_CPU_PAGE_TABLE_FALSE_POSITIVES</td>
<td>CPU page table false positives.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_0022_SWIZZLE_PATTERN</td>
<td>Swizzle pattern.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_0022_TEXTURE_LAYOUT</td>
<td>Texture layout.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_0023_UMD_BASED_COMMAND_QUEUE_PRIORITY</td>
<td>UMD-based command queue priority.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_3DPIPELINESUPPORT</td>
<td>Support for 3D pipeline.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_ARCHITECTURE_INFO</td>
<td>Architecture information.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_D3D12_OPTIONS</td>
<td>Options for D3D12.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_GPUVA_CAPS</td>
<td>GPU video acceleration capabilities.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_MEMORY_ARCHITECTURE</td>
<td>Memory architecture.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_SHADER</td>
<td>Shader.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_SWIZZLE_PATTERN</td>
<td>Swizzle pattern.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_TEXTURE_LAYOUT</td>
<td>Texture layout.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_TEXTURE_LAYOUT_SETS</td>
<td>Texture layout sets.</td>
</tr>

<tr>
<td>D3D12DDICAPS_TYPE_TEXTURE_LAYOUT1</td>
<td>Texture layout.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |