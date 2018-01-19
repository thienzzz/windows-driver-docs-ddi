---
UID : NC:d3d12umddi.PFND3D12DDI_CREATEDEVICE_0003
title : PFND3D12DDI_CREATEDEVICE_0003
author : windows-driver-content
description : The PFND3D12DDI_CREATEDEVICE_0003 function creates a graphics context that is referenced in subsequent calls.
old-location : display\pfnd3d12ddi_createdevice_0003.htm
old-project : display
ms.assetid : 5F25CFE0-00C5-45CD-8EA1-50F01BA4EA0B
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
req.alt-api : PFND3D12DDI_CREATEDEVICE_0003
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


# PFND3D12DDI_CREATEDEVICE_0003 callback function
The PFND3D12DDI_CREATEDEVICE_0003 function creates a graphics context that is referenced in subsequent calls.

## Syntax

```
PFND3D12DDI_CREATEDEVICE_0003 Pfnd3d12ddiCreatedevice0003;

HRESULT Pfnd3d12ddiCreatedevice0003(
   D3D12DDI_HADAPTER,
  CONST D3D12DDIARG_CREATEDEVICE_0003 *
)
{...}
```

## Parameters

`D3D12DDI_HADAPTER`



`*`




## Return Value

PFND3D12DDI_CREATEDEVICE_0003 returns one of the following values:
<dl>
<dt><b>S_OK</b></dt>
</dl>The graphics context was successfully created.
<dl>
<dt><b>DXGI_STATUS_NO_REDIRECTION</b></dt>
</dl>The graphics context was successfully created. However, the DirectX Graphics Infrastructure (DXGI) should not use the shared resource presentation path to effect communication with the Desktop Windows Manager (DWM). For more information about the DXGI DDI, see <a href="https://msdn.microsoft.com/3a49d7cb-984f-4e4f-a549-5c0442e1c45a">Supporting the DXGI DDI</a>.
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
                PFND3D12DDI_CREATEDEVICE_0003 could not allocate the memory that was required for it to complete.


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