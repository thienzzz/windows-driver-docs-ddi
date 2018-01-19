---
UID : NC:d3dumddi.PFND3DDDI_UNLOCK2CB
title : PFND3DDDI_UNLOCK2CB
author : windows-driver-content
description : The pfnUnlock2Cb function unlocks an allocation that was locked by a call to the pfnLock2Cb function.
old-location : display\pfnunlock2cb.htm
old-project : display
ms.assetid : 642C6A05-DA8C-453A-B1AA-030C59F32DA5
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_PTE, DXGK_PTE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnUnlock2Cb
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
req.typenames : DXGK_PTE
---


# PFND3DDDI_UNLOCK2CB callback function
The <b>pfnUnlock2Cb</b> function unlocks an allocation that was locked by a call to the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_lock2cb.md">pfnLock2Cb</a> function.

## Syntax

```
PFND3DDDI_UNLOCK2CB Pfnd3dddiUnlock2cb;

HRESULT Pfnd3dddiUnlock2cb(
  HANDLE hDevice,
  CONST D3DDDICB_UNLOCK2 *
)
{...}
```

## Parameters

`hDevice`

A handle to the display device (graphics context).

`*`




## Return Value

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |