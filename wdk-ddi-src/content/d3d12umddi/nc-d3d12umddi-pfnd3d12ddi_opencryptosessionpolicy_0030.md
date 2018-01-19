---
UID : NC:d3d12umddi.PFND3D12DDI_OPENCRYPTOSESSIONPOLICY_0030
title : PFND3D12DDI_OPENCRYPTOSESSIONPOLICY_0030
author : windows-driver-content
description : Used to open a crypto session policy.
old-location : display\pfnd3d12ddi_opencryptosessionpolicy_0030.htm
old-project : display
ms.assetid : 24B30BE0-9B7E-4946-8677-E3E727A63498
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3D11_1DDI_GETCAPTUREHANDLEDATA, D3D11_1DDI_GETCAPTUREHANDLEDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d12umddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PFND3D12DDI_OPENCRYPTOSESSIONPOLICY_0030
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


# PFND3D12DDI_OPENCRYPTOSESSIONPOLICY_0030 callback function
Used to open a crypto session policy.

## Syntax

```
PFND3D12DDI_OPENCRYPTOSESSIONPOLICY_0030 Pfnd3d12ddiOpencryptosessionpolicy0030;

HRESULT Pfnd3d12ddiOpencryptosessionpolicy0030(
  D3D12DDI_HDEVICE hDrvDevice,
  CONST D3D12DDIARG_OPEN_CRYPTO_SESSION_POLICY_0030 *pArgs,
  D3D12DDI_HCRYPTOSESSIONPOLICY_0030 hDrvCryptoSessionPolicy
)
{...}
```

## Parameters

`hDrvDevice`

The hardware device being processed.

`*pArgs`



`hDrvCryptoSessionPolicy`




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