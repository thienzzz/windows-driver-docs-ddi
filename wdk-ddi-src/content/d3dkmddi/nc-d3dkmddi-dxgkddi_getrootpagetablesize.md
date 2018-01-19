---
UID : NC:d3dkmddi.DXGKDDI_GETROOTPAGETABLESIZE
title : DXGKDDI_GETROOTPAGETABLESIZE
author : windows-driver-content
description : DxgkDdiGetRootPageTableSize returns the minimum root page table size, in bytes, that is needed to hold the given number of page table entries.
old-location : display\dxgkddigetrootpagetablesize.htm
old-project : display
ms.assetid : 474F1772-0DF9-487B-AEB9-302392AE0B98
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DD_MULTISAMPLEQUALITYLEVELSDATA, DD_MULTISAMPLEQUALITYLEVELSDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dkmddi.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DxgkDdiGetRootPageTableSize
req.alt-loc : d3dkmddi.h
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
req.typenames : DD_MULTISAMPLEQUALITYLEVELSDATA
---


# DXGKDDI_GETROOTPAGETABLESIZE function
<b>DxgkDdiGetRootPageTableSize</b> returns the minimum root page table size,  in bytes, that is needed to hold the given number of page table entries. The actual number of entries in the page table could be greater than the given value. 

<b>DxgkDdiGetRootPageTableSize</b> is called only when <b>DXGK_GPUMMUCAPS</b>::<b>PageTableLevelCount</b> is two.

## Syntax

```
DXGKDDI_GETROOTPAGETABLESIZE DxgkddiGetrootpagetablesize;

SIZE_T DxgkddiGetrootpagetablesize(
  IN_CONST_HANDLE hAdapter,
  INOUT_PDXGKARG_GETROOTPAGETABLESIZE pArgs
)
{...}
```

## Parameters

`hAdapter`

A handle to the display adapter.

`pArgs`

The <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_getrootpagetablesize.md">DXGKARG_GETROOTPAGETABLESIZE</a> structure that describes the operation.


## Return Value

The page table size in bytes. The size must be a multiple of the page size of the GPU memory segment where page table is located.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |