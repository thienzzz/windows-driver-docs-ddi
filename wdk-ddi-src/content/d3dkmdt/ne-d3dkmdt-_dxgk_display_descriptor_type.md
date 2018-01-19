---
UID : NE:d3dkmdt._DXGK_DISPLAY_DESCRIPTOR_TYPE
title : _DXGK_DISPLAY_DESCRIPTOR_TYPE
author : windows-driver-content
description : Enum used to express the display descriptor type.
old-location : display\dxgk_display_descriptor_type.htm
old-project : display
ms.assetid : 2AC0B5CF-67FB-462F-9118-E30FEDE9A019
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_DISPLAY_DESCRIPTOR_TYPE, *PDXGK_DISPLAY_DESCRIPTOR_TYPE, DXGK_DISPLAY_DESCRIPTOR_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dkmdt.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_DISPLAY_DESCRIPTOR_TYPE
req.alt-loc : d3dkmdt.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : "*PDXGK_DISPLAY_DESCRIPTOR_TYPE, DXGK_DISPLAY_DESCRIPTOR_TYPE"
---

# _DXGK_DISPLAY_DESCRIPTOR_TYPE Enumeration
Enum used to express the display descriptor type.

## Syntax
````
typedef enum _DXGK_DISPLAY_DESCRIPTOR_TYPE { 
  DXGK_DDT_INVALID  = 0,
  DXGK_DDT_EDID
} DXGK_DISPLAY_DESCRIPTOR_TYPE, *PDXGK_DISPLAY_DESCRIPTOR_TYPE ;
````

## Constants

<table>

<tr>
<td>DXGK_DDT_EDID</td>
<td>A VESA EDID descriptor.</td>
</tr>

<tr>
<td>DXGK_DDT_INVALID</td>
<td>Invalid type.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmdt.h |