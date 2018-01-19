---
UID : NE:d3d12umddi.D3D12DDI_TABLE_TYPE
title : D3D12DDI_TABLE_TYPE
author : windows-driver-content
description : Command list and queue types to allow drivers to point to different implementations for video.
old-location : display\d3d12ddi_table_type.htm
old-project : display
ms.assetid : 93562C36-7ADE-4CC6-B33D-D6E955E3D42C
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_TABLE_TYPE, D3D12DDI_TABLE_TYPE
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
req.alt-api : D3D12DDI_TABLE_TYPE
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
req.typenames : D3D12DDI_TABLE_TYPE
---

# D3D12DDI_TABLE_TYPE Enumeration
Command list and queue types to allow drivers to point to different implementations for video.

## Syntax
````
typedef enum D3D12DDI_TABLE_TYPE { 
  D3D12DDI_TABLE_TYPE_DEVICE_CORE                               = 0,
  D3D12DDI_TABLE_TYPE_COMMAND_LIST_3D                           = 1,
  D3D12DDI_TABLE_TYPE_COMMAND_QUEUE_3D                          = 2,
  D3D12DDI_TABLE_TYPE_DXGI                                      = 3,
  D3D12DDI_TABLE_TYPE_0020_DEVICE_VIDEO                         = 4,
  D3D12DDI_TABLE_TYPE_0020_DEVICE_CORE_VIDEO                    = 7,
  D3D12DDI_TABLE_TYPE_0020_EXTENDED_FEATURES                    = 8,
  D3D12DDI_TABLE_TYPE_0020_PASS_EXPERIMENT                      = 9,
  D3D12DDI_TABLE_TYPE_0021_SHADERCACHE_CALLBACKS                = 10,
  D3D12DDI_TABLE_TYPE_0022_COMMAND_QUEUE_VIDEO_DECODE           = 11,
  D3D12DDI_TABLE_TYPE_0022_COMMAND_LIST_VIDEO_DECODE            = 12,
  D3D12DDI_TABLE_TYPE_0022_COMMAND_QUEUE_VIDEO_PROCESS          = 13,
  D3D12DDI_TABLE_TYPE_0022_COMMAND_LIST_VIDEO_PROCESS           = 14,
  D3D12DDI_TABLE_TYPE_0030_DEVICE_CONTENT_PROTECTION_RESOURCES  = 15,
  D3D12DDI_TABLE_TYPE_0030_CONTENT_PROTECTION_CALLBACKS         = 16,
  D3D12DDI_TABLE_TYPE_0030_DEVICE_CONTENT_PROTECTION_STREAMING  = 17
} D3D12DDI_TABLE_TYPE;
````

## Constants

<table>

<tr>
<td>D3D12DDI_TABLE_TYPE_0020_DEVICE_CORE_VIDEO</td>
<td>Queue video.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0020_DEVICE_VIDEO</td>
<td>Device video.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0020_EXTENDED_FEATURES</td>
<td>Extended features.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0020_PASS_EXPERIMENT</td>
<td>Pass experiment.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0021_SHADERCACHE_CALLBACKS</td>
<td>Shader cache callbacks.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0022_COMMAND_LIST_VIDEO_DECODE</td>
<td>List video decode.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0022_COMMAND_LIST_VIDEO_PROCESS</td>
<td>List video process.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0022_COMMAND_QUEUE_VIDEO_DECODE</td>
<td>Queue video decode.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0022_COMMAND_QUEUE_VIDEO_PROCESS</td>
<td>Queue video process.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0030_CONTENT_PROTECTION_CALLBACKS</td>
<td>Content protection callbacks.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0030_DEVICE_CONTENT_PROTECTION_RESOURCES</td>
<td>Device content protection resources.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_0030_DEVICE_CONTENT_PROTECTION_STREAMING</td>
<td>Device content protection streaming.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_COMMAND_LIST_3D</td>
<td>List 3D.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_COMMAND_QUEUE_3D</td>
<td>Queue 3D.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_DEVICE_CORE</td>
<td>Device core.</td>
</tr>

<tr>
<td>D3D12DDI_TABLE_TYPE_DXGI</td>
<td>DXGI.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |