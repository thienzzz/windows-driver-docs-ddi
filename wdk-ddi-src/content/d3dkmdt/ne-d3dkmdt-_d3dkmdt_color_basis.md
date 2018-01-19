---
UID : NE:d3dkmdt._D3DKMDT_COLOR_BASIS
title : _D3DKMDT_COLOR_BASIS
author : windows-driver-content
description : The D3DKMDT_COLOR_BASIS enumeration contains constants that indicate the color basis used to encode the content of a video present source or the signal on a video present target.
old-location : display\d3dkmdt_color_basis.htm
old-project : display
ms.assetid : c2a8973d-bdab-44a6-b88b-482355ada1e5
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMDT_COLOR_BASIS, D3DKMDT_COLOR_BASIS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dkmdt.h
req.include-header : D3dkmdt.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMDT_COLOR_BASIS
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
req.typenames : D3DKMDT_COLOR_BASIS
---

# _D3DKMDT_COLOR_BASIS Enumeration
The D3DKMDT_COLOR_BASIS enumeration contains constants that indicate the color basis used to encode the content of a video present source or the signal on a video present target.

## Syntax
````
typedef enum _D3DKMDT_COLOR_BASIS { 
  D3DKMDT_CB_UNINITIALIZED  = 0,
  D3DKMDT_CB_INTENSITY      = 1,
  D3DKMDT_CB_SRGB           = 2,
  D3DKMDT_CB_SCRGB          = 3,
  D3DKMDT_CB_YCBCR          = 4,
  D3DKMDT_CB_YPBPR          = 5
} D3DKMDT_COLOR_BASIS;
````

## Constants

<table>

<tr>
<td>D3DKMDT_CB_INTENSITY</td>
<td>Indicates an encoding scheme that relies only on intensity. This basis is used for monochrome images.</td>
</tr>

<tr>
<td>D3DKMDT_CB_SCRGB</td>
<td>Indicates the SCRGB color basis.</td>
</tr>

<tr>
<td>D3DKMDT_CB_SRGB</td>
<td>Indicates the SRGB color basis.</td>
</tr>

<tr>
<td>D3DKMDT_CB_UNINITIALIZED</td>
<td>Indicates that a variable of type D3DKMDT_COLOR_BASIS has not yet been assigned a meaningful value.</td>
</tr>

<tr>
<td>D3DKMDT_CB_YCBCR</td>
<td>Indicates the YCBCR color basis.</td>
</tr>

<tr>
<td>D3DKMDT_CB_YPBPR</td>
<td>Indicates the YPBPR color basis.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmdt.h (include D3dkmdt.h) |