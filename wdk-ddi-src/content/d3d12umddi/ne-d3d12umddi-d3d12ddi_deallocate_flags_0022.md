---
UID : NE:d3d12umddi.D3D12DDI_DEALLOCATE_FLAGS_0022
title : D3D12DDI_DEALLOCATE_FLAGS_0022
author : windows-driver-content
description : Defines flags for use in deallocation.
old-location : display\d3d12ddi_deallocate_flags_0022.htm
old-project : display
ms.assetid : 17E3C01A-0716-4B3C-B4B3-72B055FB40EA
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_DEALLOCATE_FLAGS_0022, D3D12DDI_DEALLOCATE_FLAGS_0022
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
req.alt-api : D3D12DDI_DEALLOCATE_FLAGS_0022
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
req.typenames : D3D12DDI_DEALLOCATE_FLAGS_0022
---

# D3D12DDI_DEALLOCATE_FLAGS_0022 Enumeration
Defines flags for use in deallocation.

## Syntax
````
typedef enum D3D12DDI_DEALLOCATE_FLAGS_0022 { 
  D3D12DDI_DEALLOCATE_FLAGS_0022_NONE                 = 0x0,
  D3D12DDI_DEALLOCATE_FLAGS_0022_ASSUME_NOT_IN_USE    = 0x1,
  D3D12DDI_DEALLOCATE_FLAGS_0022_SYNCHRONOUS_DESTROY  = 0x2
} D3D12DDI_DEALLOCATE_FLAGS_0022;
````

## Constants

<table>

<tr>
<td>D3D12DDI_DEALLOCATE_FLAGS_0022_ASSUME_NOT_IN_USE</td>
<td>Assume that the allocation is not in use.</td>
</tr>

<tr>
<td>D3D12DDI_DEALLOCATE_FLAGS_0022_NONE</td>
<td>No flag value.</td>
</tr>

<tr>
<td>D3D12DDI_DEALLOCATE_FLAGS_0022_SYNCHRONOUS_DESTROY</td>
<td>Perform synchronous destroy.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |