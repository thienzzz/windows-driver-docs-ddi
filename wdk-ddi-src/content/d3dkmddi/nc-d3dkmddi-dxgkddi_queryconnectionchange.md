---
UID : NC:d3dkmddi.DXGKDDI_QUERYCONNECTIONCHANGE
title : DXGKDDI_QUERYCONNECTIONCHANGE
author : windows-driver-content
description : The OS calls this in response to a status change reported through DxgkCbIndicateConnectorChange or when the OutputFlags.ConnectorStatusChanges field indicates that a call to SetTimingsFromVidPn has detected connector status changes.
old-location : display\dxgkddi_queryconnectionchange.htm
old-project : display
ms.assetid : 8C09B692-3439-4ACD-942D-F7A107E2B4DA
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
req.alt-api : DXGKDDI_QUERYCONNECTIONCHANGE
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


# DXGKDDI_QUERYCONNECTIONCHANGE function
The OS calls this in response to a status change reported through DxgkCbIndicateConnectorChange or when the OutputFlags.ConnectorStatusChanges field indicates that a call to SetTimingsFromVidPn has detected connector status changes.

## Syntax

```
DXGKDDI_QUERYCONNECTIONCHANGE DxgkddiQueryconnectionchange;

NTSTATUS DxgkddiQueryconnectionchange(
  IN_CONST_HANDLE hAdapter,
  IN_PDXGKARG_QUERYCONNECTIONCHANGE pQueryConnectionChange
)
{...}
```

## Parameters

`hAdapter`

A handle that identifies the adapter.

`pQueryConnectionChange`

A pointer to a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryconnectionchange.md">DXGKARG_QUERYCONNECTIONCHANGE</a> structure that provides the OS allocated buffer into which the oldest change should be copied by the driver. The oldest change is judged by lowest ConnectionChangeId.


## Return Value

<dl>
<dt>STATUS_SUCCESS</dt>
</dl>Returned if the routine succeeds and returns the requested change.
<dl>
<dt>STATUS_ALREADY_COMPLETE</dt>
</dl>Returned if the routine succeeds, but the changes have already been reported to the OS.

## Remarks

This function is always called at PASSIVE level so the supporting code should be made pageable.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |