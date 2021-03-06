---
UID: NC:dispmprt.DXGK_BRIGHTNESS_GET_NIT_RANGES
title: DXGK_BRIGHTNESS_GET_NIT_RANGES
author: windows-driver-content
description:
ms.assetid: 8c36880d-c3e2-4aac-9904-5abf5cd0e6bc
ms.author: windowsdriverdev
ms.date:
ms.topic: callback
ms.prod: windows-hardware
ms.technology: windows-devices
req.header: dispmprt.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.irql:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topictype:
-	apiref
apitype:
-	UserDefined
apilocation:
-	dispmprt.h
apiname:
-	DXGK_BRIGHTNESS_GET_NIT_RANGES
product: Windows
targetos: Windows
---

# DXGK_BRIGHTNESS_GET_NIT_RANGES callback function

## -description

Implemented by the client driver to retrieve a list of supported nit ranges.

## -prototype

```
//Declaration

DXGK_BRIGHTNESS_GET_NIT_RANGES DxgkBrightnessGetNitRanges;

// Definition

NTSTATUS DxgkBrightnessGetNitRanges
(
	PVOID Context
	ULONG ChildUid
	PDXGK_BRIGHTNESS_GET_NIT_RANGES_OUT pOut
)
{...}

DXGK_BRIGHTNESS_GET_NIT_RANGES


```

## -parameters

### -param Context

[in] Context pointer provided when querying the interface.

### -param ChildUid

[in] An integer that uniquely identifies the child device. The display miniport driver's [DxgkDdiQueryChildRelations](..\dispmprt\nc-dispmprt-dxgkddi_query_child_relations.md) function previously provided this identifier to the display port driver.

### -param pOut:

[out] A pointer to a [DXGK_BRIGHTNESS_GET_NIT_RANGES_OUT](..\d3dkmdt\ns-d3dkmdt-_dxgk_brightness_get_nit_ranges_out.md) structure that represents the supported brightness ranges of the display panel.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS Values error code defined in ntstatus.h.

