---
UID : NE:d3dkmthk._D3DKMT_VIDSCHESCAPETYPE
title : _D3DKMT_VIDSCHESCAPETYPE
author : windows-driver-content
description : The D3DKMT_VIDMMESCAPETYPE enumeration is used with the D3DKMT_VIDSCH_ESCAPE structure.
old-location : display\d3dkmt_vidschescapetype.htm
old-project : display
ms.assetid : 8388A03F-995A-4A33-B541-4FF2422DEE83
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_VIDSCHESCAPETYPE, D3DKMT_VIDSCHESCAPETYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dkmthk.h
req.include-header : TBD
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMT_VIDSCHESCAPETYPE
req.alt-loc : d3dkmthk.h
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
req.typenames : D3DKMT_VIDSCHESCAPETYPE
---

# _D3DKMT_VIDSCHESCAPETYPE Enumeration
<b>Do not use the D3DKMT_VIDSCHESCAPETYPE enumeration; it is for testing purposes only.</b>

The D3DKMT_VIDMMESCAPETYPE enumeration is used with the <a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_vidsch_escape.md">D3DKMT_VIDSCH_ESCAPE</a> structure.

## Syntax
````
typedef enum _D3DKMT_VIDSCHESCAPETYPE { 
  D3DKMT_VIDSCHESCAPETYPE_PREEMPTIONCONTROL    = 0,
  D3DKMT_VIDSCHESCAPETYPE_SUSPENDSCHEDULER     = 1,
  D3DKMT_VIDSCHESCAPETYPE_TDRCONTROL           = 2,
  D3DKMT_VIDSCHESCAPETYPE_SUSPENDRESUME        = 3,
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WIN8)
  D3DKMT_VIDSCHESCAPETYPE_ENABLECONTEXTDELAY   = 4,
#endif 
  D3DKMT_VIDSCHESCAPETYPE_CONFIGURE_TDR_LIMIT  = 5
} D3DKMT_VIDSCHESCAPETYPE;
````

## Constants

<table>

<tr>
<td>D3DKMT_VIDSCHESCAPETYPE_CONFIGURE_TDR_LIMIT</td>
<td></td>
</tr>

<tr>
<td>D3DKMT_VIDSCHESCAPETYPE_ENABLECONTEXTDELAY</td>
<td></td>
</tr>

<tr>
<td>D3DKMT_VIDSCHESCAPETYPE_PREEMPTIONCONTROL</td>
<td></td>
</tr>

<tr>
<td>D3DKMT_VIDSCHESCAPETYPE_SUSPENDRESUME</td>
<td></td>
</tr>

<tr>
<td>D3DKMT_VIDSCHESCAPETYPE_SUSPENDSCHEDULER</td>
<td></td>
</tr>

<tr>
<td>D3DKMT_VIDSCHESCAPETYPE_TDRCONTROL</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h (include TBD) |