---
UID: NS:d3dkmthk._DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2
title: _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2
author: windows-driver-content
description:
ms.assetid: e312c3ba-7a23-41e4-bebb-b19daa7a43ae
ms.author: windowsdriverdev
ms.date:
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2, DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT, DXGK_GRAPHICSPOWER_REGISTER_INPUT
req.header: d3dkmthk.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.ddi-compliance:
req.unicode-ansi:
req.max-support:
req.typenames: DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2, *PDXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2
topictype:
-	apiref
apitype:
-	HeaderDef
apilocation:
-	d3dkmthk.h
apiname:
-	_DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2
product: Windows
targetos: Windows
---

# _DXGK_GRAPHICSPOWER_REGISTER_INPUT_V_1_2 structure

## -description

Used to register the power state of a new input.

## -struct-fields

### -field Version

The current version being used.

### -field PrivateHandle

A private handle to the device.

### -field PowerNotificationCb

Issues a power notification.

### -field RemovalNotificationCb

Issues a removal notification.

### -field FStateNotificationCb

Issues a state notification.

### -field InitialComponentStateCb

Initializes the component state.

