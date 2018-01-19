---
UID : NE:d3d12umddi.D3D12DDI_QUERY_TYPE
title : D3D12DDI_QUERY_TYPE
author : windows-driver-content
description : Type of a query.
old-location : display\d3d12ddi_query_type.htm
old-project : display
ms.assetid : C411997A-0F01-4D88-816A-BD375D0744C7
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_QUERY_TYPE, D3D12DDI_QUERY_TYPE
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
req.alt-api : D3D12DDI_QUERY_TYPE
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
req.typenames : D3D12DDI_QUERY_TYPE
---

# D3D12DDI_QUERY_TYPE Enumeration
Type of a query.

## Syntax
````
typedef enum D3D12DDI_QUERY_TYPE { 
  D3D12DDI_QUERY_TYPE_OCCLUSION                     = 0,
  D3D12DDI_QUERY_TYPE_BINARY_OCCLUSION              = 1,
  D3D12DDI_QUERY_TYPE_TIMESTAMP                     = 2,
  D3D12DDI_QUERY_TYPE_PIPELINE_STATISTICS           = 3,
  D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM0         = 4,
  D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM1         = 5,
  D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM2         = 6,
  D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM3         = 7,
  D3D12DDI_QUERY_TYPE_0020_VIDEO_DECODE_STATISTICS  = 8
} D3D12DDI_QUERY_TYPE;
````

## Constants

<table>

<tr>
<td>D3D12DDI_QUERY_TYPE_0020_VIDEO_DECODE_STATISTICS</td>
<td>Video decode statistics.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_BINARY_OCCLUSION</td>
<td>Binary occlusion.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_OCCLUSION</td>
<td>Occlusion.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_PIPELINE_STATISTICS</td>
<td>Pipeline statistics.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM0</td>
<td>SO statistics for Stream0.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM1</td>
<td>SO statistics for Stream1.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM2</td>
<td>SO statistics for Stream2.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_SO_STATISTICS_STREAM3</td>
<td>SO statistics for Stream3.</td>
</tr>

<tr>
<td>D3D12DDI_QUERY_TYPE_TIMESTAMP</td>
<td>Timestamp.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |