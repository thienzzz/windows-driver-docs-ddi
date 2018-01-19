---
UID : NE:d3dkmddi._DXGK_DISPLAYPANELORIENTATION
title : _DXGK_DISPLAYPANELORIENTATION
author : windows-driver-content
description : Enum used to express the orientation of an integrated panel.
old-location : display\dxgk_displaypanelorientation.htm
old-project : display
ms.assetid : 49758A57-EFCE-4E9C-9BF6-74F6EFD356D9
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_DISPLAYPANELORIENTATION, DXGK_DISPLAYPANELORIENTATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dkmddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_DISPLAYPANELORIENTATION
req.alt-loc : d3dkmddi.h
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
req.typenames : DXGK_DISPLAYPANELORIENTATION
---

# _DXGK_DISPLAYPANELORIENTATION Enumeration
Enum used to express the orientation of an integrated panel.

## Syntax
````
typedef enum _DXGK_DISPLAYPANELORIENTATION { 
  DXGK_DPO_0    = 0,
  DXGK_DPO_90   = 1,
  DXGK_DPO_180  = 2,
  DXGK_DPO_270  = 3
} DXGK_DISPLAYPANELORIENTATION;
````

## Constants

<table>

<tr>
<td>DXGK_DPO_0</td>
<td>Indicates a 0 degree rotation.</td>
</tr>

<tr>
<td>DXGK_DPO_180</td>
<td>Indicates a 180 degree rotation.</td>
</tr>

<tr>
<td>DXGK_DPO_270</td>
<td>Indicates a 270 degree rotation.</td>
</tr>

<tr>
<td>DXGK_DPO_90</td>
<td>Indicates a 90 degree rotation.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |