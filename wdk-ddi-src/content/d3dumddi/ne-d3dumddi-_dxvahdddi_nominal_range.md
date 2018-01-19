---
UID : NE:d3dumddi._DXVAHDDDI_NOMINAL_RANGE
title : _DXVAHDDDI_NOMINAL_RANGE
author : windows-driver-content
description : Indicates the luminance range of YUV data.
old-location : display\dxvahdddi_nominal_range.htm
old-project : display
ms.assetid : 952BE36C-0F53-47C3-9C95-E6ECAB9D36D1
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXVAHDDDI_NOMINAL_RANGE, DXVAHDDDI_NOMINAL_RANGE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXVAHDDDI_NOMINAL_RANGE
req.alt-loc : D3dumddi.h
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
req.typenames : DXVAHDDDI_NOMINAL_RANGE
---

# _DXVAHDDDI_NOMINAL_RANGE Enumeration
Indicates the luminance range of YUV data.

## Syntax
````
typedef enum _DXVAHDDDI_NOMINAL_RANGE { 
  DXVAHDDDI_NOMINAL_RANGE_UNDEFINED  = 0,
  DXVAHDDDI_NOMINAL_RANGE_16_235     = 1,
  DXVAHDDDI_NOMINAL_RANGE_0_255      = 2
} DXVAHDDDI_NOMINAL_RANGE;
````

## Constants

<table>

<tr>
<td>DXVAHDDDI_NOMINAL_RANGE_0_255</td>
<td>The <i>full luminance range</i>, or <i>extended range</i>, of 0 to 255, inclusive [0, 255].</td>
</tr>

<tr>
<td>DXVAHDDDI_NOMINAL_RANGE_16_235</td>
<td>The <i>studio luminance range</i> of 16 to 235, inclusive [16, 235].</td>
</tr>

<tr>
<td>DXVAHDDDI_NOMINAL_RANGE_UNDEFINED</td>
<td>The driver default value, which is the <i>studio luminance range</i> of 16 to 235, inclusive [16, 235].</td>
</tr>
</table>

## Remarks

For more information on luminance range, see <a href="https://msdn.microsoft.com/D76FFB8C-CA42-446E-826F-52982B1849E5">YUV format ranges in Windows 8.1</a>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |