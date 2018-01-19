---
UID : NC:d3d12umddi.PFND3D12DDI_CREATE_PROTECTED_SESSION_CB_0030
title : PFND3D12DDI_CREATE_PROTECTED_SESSION_CB_0030
author : windows-driver-content
description : Used to create a protected session state.
old-location : display\pfnd3d12ddi_create_protected_session_cb_0030.htm
old-project : display
ms.assetid : 64E38759-2863-4481-8A89-6E6263CEFE8B
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
req.alt-api : PFND3D12DDI_CREATE_PROTECTED_SESSION_CB_0030
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


# PFND3D12DDI_CREATE_PROTECTED_SESSION_CB_0030 callback function
Used to create a protected session state.

## Syntax

```
PFND3D12DDI_CREATE_PROTECTED_SESSION_CB_0030 Pfnd3d12ddiCreateProtectedSessionCb0030;

HRESULT Pfnd3d12ddiCreateProtectedSessionCb0030(
  D3D12DDI_HRTDEVICE hRTDevice,
  D3D12DDI_HRTPROTECTEDSESSION_0030 hRTProtectedSession,
  D3D12DDICB_CREATE_PROTECTED_RESOURCE_SESSION *pArgs
)
{...}
```

## Parameters

`hRTDevice`

The hardware device being processed.

`hRTProtectedSession`

The protected session.

`*pArgs`




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