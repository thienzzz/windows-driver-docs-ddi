---
UID : NE:d3d10umddi.D3DWDDM1_3DDI_TILE_MAPPING_FLAG
title : D3DWDDM1_3DDI_TILE_MAPPING_FLAG
author : windows-driver-content
description : Indicates how to update a tile mapping.
old-location : display\d3dwddm1_3ddi_tile_mapping_flag.htm
old-project : display
ms.assetid : 1149547D-9165-42AA-B12A-5C7681A8EAC1
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3DWDDM1_3DDI_TILE_MAPPING_FLAG, D3DWDDM1_3DDI_TILE_MAPPING_FLAG
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1,WDDM 1.3
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DWDDM1_3DDI_TILE_MAPPING_FLAG
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
req.typenames : D3DWDDM1_3DDI_TILE_MAPPING_FLAG
---

# D3DWDDM1_3DDI_TILE_MAPPING_FLAG Enumeration
Indicates how to update a tile mapping.

## Syntax
````
enum D3DWDDM1_3DDI_TILE_MAPPING_FLAG {
  D3DWDDM1_3DDI_TILE_MAPPING_NO_OVERWRITE  = 0x00000001 

};
````

## Constants

<table>

<tr>
<td>D3DWDDM1_3DDI_TILE_MAPPING_NO_OVERWRITE</td>
<td>Previously submitted commands to the 
device that may still be executing do not reference any of the tile region being updated.
This allows the device to avoid having to flush previously submitted work in order to update a tile mapping.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |