---
UID : NC:d3dumddi.PFND3DDDI_LOGUMDMARKERCB
title : PFND3DDDI_LOGUMDMARKERCB
author : windows-driver-content
description : Called by the user-mode display driver to log a custom Event Tracing for Windows (ETW) marker event.
old-location : display\pfnlogumdmarkercb.htm
old-project : display
ms.assetid : BD544686-20D3-4577-9950-9C3B6853C4BD
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_PTE, DXGK_PTE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dumddi.h
req.include-header : D3d10umddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 8.1,WDDM 1.3 and later
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnLogUMDMarkerCb
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
req.typenames : DXGK_PTE
---


# PFND3DDDI_LOGUMDMARKERCB callback function
Called by the user-mode display driver to log a custom Event Tracing for Windows (ETW) marker event.

## Syntax

```
PFND3DDDI_LOGUMDMARKERCB Pfnd3dddiLogumdmarkercb;

HRESULT Pfnd3dddiLogumdmarkercb(
  HANDLE hDevice,
  CONST D3DDDICB_LOGUMDMARKER *
)
{...}
```

## Parameters

`hDevice`

A handle to the display device (graphics context).

`*`




## Return Value

Returns <b>S_OK</b> or an appropriate error result if the function does not complete successfully.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3d10umddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |