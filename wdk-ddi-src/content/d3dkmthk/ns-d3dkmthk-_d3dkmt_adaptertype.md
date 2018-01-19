---
UID : NS:d3dkmthk._D3DKMT_ADAPTERTYPE
title : _D3DKMT_ADAPTERTYPE
author : windows-driver-content
description : Specifies the type of display device that the graphics adapter supports.
old-location : display\d3dkmt_adaptertype.htm
old-project : display
ms.assetid : a92865bc-620f-434d-a185-b837924599fc
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_ADAPTERTYPE, D3DKMT_ADAPTERTYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmthk.h
req.include-header : D3dkmthk.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMT_ADAPTERTYPE
req.alt-loc : D3dkmthk.h
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
req.typenames : D3DKMT_ADAPTERTYPE
---

# _D3DKMT_ADAPTERTYPE structure
Specifies the type of display device that the graphics adapter supports.

## Syntax
````
typedef struct _D3DKMT_ADAPTERTYPE {
  UINT RenderSupported  :1;
  UINT DisplaySupported  :1;
  UINT SoftwareDevice  :1;
  UINT PostDevice  :1;
  UINT Reserved  :28;
} D3DKMT_ADAPTERTYPE;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h (include D3dkmthk.h) |