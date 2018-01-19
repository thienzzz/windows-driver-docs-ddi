---
UID : NE:d3dkmdt._D3DKMDT_MONITOR_DESCRIPTOR_TYPE
title : _D3DKMDT_MONITOR_DESCRIPTOR_TYPE
author : windows-driver-content
description : The D3DKMDT_MONITOR_DESCRIPTOR_TYPE enumeration is used to indicate a particular type of monitor descriptor.
old-location : display\d3dkmdt_monitor_descriptor_type.htm
old-project : display
ms.assetid : f5ec761f-fc20-4baf-a012-c32356644a6c
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMDT_MONITOR_DESCRIPTOR_TYPE, D3DKMDT_MONITOR_DESCRIPTOR_TYPE
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
req.alt-api : D3DKMDT_MONITOR_DESCRIPTOR_TYPE
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
req.typenames : D3DKMDT_MONITOR_DESCRIPTOR_TYPE
---

# _D3DKMDT_MONITOR_DESCRIPTOR_TYPE Enumeration
The D3DKMDT_MONITOR_DESCRIPTOR_TYPE enumeration is used to indicate a particular type of monitor descriptor.

## Syntax
````
typedef enum _D3DKMDT_MONITOR_DESCRIPTOR_TYPE { 
  D3DKMDT_MDT_UNINITIALIZED           = 0,
  D3DKMDT_MDT_VESA_EDID_V1_BASEBLOCK  = 1,
  D3DKMDT_MDT_VESA_EDID_V1_BLOCKMAP   = 2,
  D3DKMDT_MDT_OTHER                   = 255
} D3DKMDT_MONITOR_DESCRIPTOR_TYPE;
````

## Constants

<table>

<tr>
<td>D3DKMDT_MDT_OTHER</td>
<td>Indicates that the descriptor has a type other than those indicated by the previous values of this enumeration.</td>
</tr>

<tr>
<td>D3DKMDT_MDT_UNINITIALIZED</td>
<td>Indicates that a variable of type D3DKMDT_MONITOR_DESCRIPTOR_TYPE has not yet been assigned a meaningful value.</td>
</tr>

<tr>
<td>D3DKMDT_MDT_VESA_EDID_V1_BASEBLOCK</td>
<td>Indicates that the descriptor is an Extended Display Identification Data (EDID) base block.</td>
</tr>

<tr>
<td>D3DKMDT_MDT_VESA_EDID_V1_BLOCKMAP</td>
<td>Indicates that the descriptor is an EDID block map.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmdt.h (include D3dkmdt.h) |