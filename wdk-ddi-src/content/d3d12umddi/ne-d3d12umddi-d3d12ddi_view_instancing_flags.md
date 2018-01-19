---
UID : NE:d3d12umddi.D3D12DDI_VIEW_INSTANCING_FLAGS
title : D3D12DDI_VIEW_INSTANCING_FLAGS
author : windows-driver-content
description : Defines the view instancing flags.
old-location : display\d3d12ddi-view-instancing-flags.htm
old-project : display
ms.assetid : fa44933f-aa3b-466a-8ee2-2d34d0311562
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_VIEW_INSTANCING_FLAGS, D3D12DDI_VIEW_INSTANCING_FLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d12umddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D12DDI_VIEW_INSTANCING_FLAGS
req.alt-loc : d3d12umddi.h
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
req.typenames : D3D12DDI_VIEW_INSTANCING_FLAGS
---

# D3D12DDI_VIEW_INSTANCING_FLAGS Enumeration
Defines the view instancing flags.

## Syntax
````
typedef enum _D3D12DDI_VIEW_INSTANCING_FLAGS { 
  D3D12DDI_VIEW_INSTANCING_FLAG_NONE,
  D3D12DDI_VIEW_INSTANCING_FLAG_ENABLE_VIEW_INSTANCE_MASKING
} D3D12DDI_VIEW_INSTANCING_FLAGS;
````

## Constants

<table>

<tr>
<td>D3D12DDI_VIEW_INSTANCING_FLAG_ENABLE_VIEW_INSTANCE_MASKING</td>
<td>The view instancing flag is enable view instance masking.</td>
</tr>

<tr>
<td>D3D12DDI_VIEW_INSTANCING_FLAG_NONE</td>
<td>No view instancing flag is defined.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h |