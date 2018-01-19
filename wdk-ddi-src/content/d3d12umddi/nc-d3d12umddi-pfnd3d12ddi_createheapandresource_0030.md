---
UID : NC:d3d12umddi.PFND3D12DDI_CREATEHEAPANDRESOURCE_0030
title : PFND3D12DDI_CREATEHEAPANDRESOURCE_0030
author : windows-driver-content
description : Used to simultaneously create a heap and resource.
old-location : display\pfnd3d12ddi_createheapandresource_0030.htm
old-project : display
ms.assetid : A6D597AA-C72A-46A5-91E8-22B225B380F2
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3D11_1DDI_GETCAPTUREHANDLEDATA, D3D11_1DDI_GETCAPTUREHANDLEDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d12umddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PFND3D12DDI_CREATEHEAPANDRESOURCE_0030
req.alt-loc : d3d12umddi.h
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
req.typenames : D3D11_1DDI_GETCAPTUREHANDLEDATA
---


# PFND3D12DDI_CREATEHEAPANDRESOURCE_0030 callback function
<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Used to simultaneously create a heap and resource.

## Syntax

```
PFND3D12DDI_CREATEHEAPANDRESOURCE_0030 Pfnd3d12ddiCreateheapandresource0030;

HRESULT Pfnd3d12ddiCreateheapandresource0030(
   D3D12DDI_HDEVICE,
  CONST D3D12DDIARG_CREATEHEAP_0001 *,
   D3D12DDI_HHEAP,
   D3D12DDI_HRTRESOURCE,
  CONST D3D12DDIARG_CREATERESOURCE_0003 *,
  CONST D3D12DDI_CLEAR_VALUES *,
   D3D12DDI_HPROTECTEDRESOURCESESSION_0030,
   D3D12DDI_HRESOURCE
)
{...}
```

## Parameters

`D3D12DDI_HDEVICE`



`*`



`D3D12DDI_HHEAP`



`D3D12DDI_HRTRESOURCE`



`*`



`*`



`D3D12DDI_HPROTECTEDRESOURCESESSION_0030`



`D3D12DDI_HRESOURCE`




## Return Value

Returns STATUS_SUCCESS if completed successfully.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |