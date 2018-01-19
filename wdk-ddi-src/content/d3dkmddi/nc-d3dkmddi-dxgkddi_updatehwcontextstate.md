---
UID : NC:d3dkmddi.DXGKDDI_UPDATEHWCONTEXTSTATE
title : DXGKDDI_UPDATEHWCONTEXTSTATE
author : windows-driver-content
description : Used to update the hardware context state.
old-location : display\dxgkddi_updatehwcontextstate.htm
old-project : display
ms.assetid : 1187A302-CD7D-418E-B48F-74D1FF29C991
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DD_MULTISAMPLEQUALITYLEVELSDATA, DD_MULTISAMPLEQUALITYLEVELSDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dkmddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGKDDI_UPDATEHWCONTEXTSTATE
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
req.irql : requires_(PASSIVE_LEVEL)
req.typenames : DD_MULTISAMPLEQUALITYLEVELSDATA
---


# DXGKDDI_UPDATEHWCONTEXTSTATE function
Used to update the hardware context state.

## Syntax

```
DXGKDDI_UPDATEHWCONTEXTSTATE DxgkddiUpdatehwcontextstate;

NTSTATUS DxgkddiUpdatehwcontextstate(
  IN_CONST_HANDLE hAdapter,
  IN_CONST_PDXGKARG_UPDATEHWCONTEXTSTATE pUpdateHwContextState
)
{...}
```

## Parameters

`hAdapter`

A handle to the generated adapter.

`pUpdateHwContextState`

A pointer used by the function to update the hardware context state.


## Return Value

Returns STATUS_SUCCESS if completed successfully.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |
| **Library** |  |
| **IRQL** | requires_(PASSIVE_LEVEL) |
| **DDI compliance rules** |  |