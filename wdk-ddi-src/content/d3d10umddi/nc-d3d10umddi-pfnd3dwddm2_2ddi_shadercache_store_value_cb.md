---
UID : NC:d3d10umddi.PFND3DWDDM2_2DDI_SHADERCACHE_STORE_VALUE_CB
title : PFND3DWDDM2_2DDI_SHADERCACHE_STORE_VALUE_CB
author : windows-driver-content
description : The pfnShaderCacheStoreValue callback function stores a shader cache value.
old-location : display\pfnd3dwddm2_2ddi_shadercache_store_value.htm
old-project : display
ms.assetid : 715D4C28-029F-463E-9A6D-D8155B570538
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _SETRESULT_INFO, *PSETRESULT_INFO, SETRESULT_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnShaderCacheStoreValue
req.alt-loc : D3d12umddi.h
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
req.typenames : "*PSETRESULT_INFO, SETRESULT_INFO"
---


# PFND3DWDDM2_2DDI_SHADERCACHE_STORE_VALUE_CB callback function
The <i>pfnShaderCacheStoreValue</i> callback function stores a shader cache value.

## Syntax

```
PFND3DWDDM2_2DDI_SHADERCACHE_STORE_VALUE_CB Pfnd3dwddm22DdiShadercacheStoreValueCb;

HRESULT Pfnd3dwddm22DdiShadercacheStoreValueCb(
  D3DWDDM2_2DDI_HRTCACHESESSION hCacheSession,
  const D3DWDDM2_2DDI_SHADERCACHE_HASH *pPrecomputedHash,
  const void *pKey,
  SIZE_T KeyLen,
  const void *pValue,
  SIZE_T ValueLen
)
{...}
```

## Parameters

`hCacheSession`

The handle of the cache session for the driver to use when it calls back into the runtime.

`*pPrecomputedHash`



`*pKey`



`KeyLen`

The length of the key.

`*pValue`



`ValueLen`

The length of the input value.


## Return Value

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |