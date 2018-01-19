---
UID : NC:d3d12umddi.PFND3D12DDI_GETKEYBASEDATA_0030
title : PFND3D12DDI_GETKEYBASEDATA_0030
author : windows-driver-content
description : Used to get key base data.
old-location : display\pfnd3d12ddi_getkeybasedata_0030.htm
old-project : display
ms.assetid : D4F893E9-6B7B-4E35-A92F-B31FFD55A2C0
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
req.alt-api : PFND3D12DDI_GETKEYBASEDATA_0030
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


# PFND3D12DDI_GETKEYBASEDATA_0030 callback function
Used to get key base data.

## Syntax

```
PFND3D12DDI_GETKEYBASEDATA_0030 Pfnd3d12ddiGetkeybasedata0030;

HRESULT Pfnd3d12ddiGetkeybasedata0030(
  D3D12DDI_HDEVICE hDrvDevice,
  D3D12DDI_HCRYPTOSESSION_0030 hDrvCryptoSession,
  CONST VOID *pKeyInputData,
  UINT KeyInputDataSize,
  VOID *pKeyBaseData,
  UINT KeyBaseDataSize
)
{...}
```

## Parameters

`hDrvDevice`

The device being processed.

`hDrvCryptoSession`

The crypto session.

`*pKeyInputData`



`KeyInputDataSize`

The size of the key input data.

`*pKeyBaseData`



`KeyBaseDataSize`

The size of the key base data.


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