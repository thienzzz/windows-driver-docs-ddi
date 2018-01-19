---
UID : NE:d3dumddi._DXVAHDDDI_DEVICE_USAGE
title : _DXVAHDDDI_DEVICE_USAGE
author : windows-driver-content
description : The DXVAHDDDI_DEVICE_USAGE enumeration contains values that identify how the decode device plays video.
old-location : display\dxvahdddi_device_usage.htm
old-project : display
ms.assetid : 9a2e74fa-ee02-46f9-a51e-b2ffcdf7617a
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXVAHDDDI_DEVICE_USAGE, DXVAHDDDI_DEVICE_USAGE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : DXVAHDDDI_DEVICE_USAGE is supported beginning with the Windows 7 operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXVAHDDDI_DEVICE_USAGE
req.alt-loc : d3dumddi.h
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
req.typenames : DXVAHDDDI_DEVICE_USAGE
---

# _DXVAHDDDI_DEVICE_USAGE Enumeration
The DXVAHDDDI_DEVICE_USAGE enumeration contains values that identify how the decode device plays video.

## Syntax
````
typedef enum _DXVAHDDDI_DEVICE_USAGE { 
  DXVAHDDDI_DEVICE_USAGE_PLAYBACK_NORMAL  = 0,
  DXVAHDDDI_DEVICE_USAGE_OPTIMAL_SPEED    = 1,
  DXVAHDDDI_DEVICE_USAGE_OPTIMAL_QUALITY  = 2
} DXVAHDDDI_DEVICE_USAGE;
````

## Constants

<table>

<tr>
<td>DXVAHDDDI_DEVICE_USAGE_OPTIMAL_QUALITY</td>
<td>A value that specifies that the device plays video at optimal quality.</td>
</tr>

<tr>
<td>DXVAHDDDI_DEVICE_USAGE_OPTIMAL_SPEED</td>
<td>A value that specifies that the device plays video at optimal speed.</td>
</tr>

<tr>
<td>DXVAHDDDI_DEVICE_USAGE_PLAYBACK_NORMAL</td>
<td>A value that specifies that the device plays video at normal speed.</td>
</tr>
</table>

## Remarks

A DXVAHDDDI_DEVICE_USAGE-typed value is specified in the <b>Usage</b> member of a <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_device_desc.md">DXVAHDDDI_DEVICE_DESC</a> structure to help describe a decode device.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |

## See Also

<dl>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_device_desc.md">DXVAHDDDI_DEVICE_DESC</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXVAHDDDI_DEVICE_USAGE enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>