---
UID : NC:usbcamdi.PCAM_NEW_FRAME_ROUTINE_EX
title : PCAM_NEW_FRAME_ROUTINE_EX
author : windows-driver-content
description : A camera minidriver's CamNewVideoFrameEx callback function initializes a new video frame context structure.
old-location : stream\camnewvideoframeex.htm
old-project : stream
ms.assetid : 739e434e-9621-4927-bf1d-2e7c3b2828d7
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : _USB_BUS_INTERFACE_USBDI_V3, USB_BUS_INTERFACE_USBDI_V3, *PUSB_BUS_INTERFACE_USBDI_V3
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : usbcamdi.h
req.include-header : Usbcamdi.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : CamNewVideoFrameEx
req.alt-loc : usbcamdi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : DISPATCH_LEVEL (See Remarks section)
req.typenames : USB_BUS_INTERFACE_USBDI_V3, *PUSB_BUS_INTERFACE_USBDI_V3
req.product : Windows 10 or later.
---


# PCAM_NEW_FRAME_ROUTINE_EX callback function
A camera minidriver's <b>CamNewVideoFrameEx</b> callback function initializes a new video frame context structure.

## Syntax

```
PCAM_NEW_FRAME_ROUTINE_EX PcamNewFrameRoutineEx;

void PcamNewFrameRoutineEx(
  PVOID DeviceContext,
  PVOID FrameContext,
  ULONG StreamNumber,
  PULONG FrameLength
)
{...}
```

## Parameters

`DeviceContext`

Specifies the minidriver device context.

`FrameContext`

Specifies the frame context to be initialized.

`StreamNumber`

Indicates the stream associated with this new frame.

`FrameLength`

Pointer to the raw frame buffer length. The length is expressed in bytes. The camera minidriver may decrease this value if it does not require a buffer transfer on the USB bus of the specified size. The camera minidriver should not increase this value.


## Return Value

<b>CamNewVideoFrameEx</b> does not return a value.

## Remarks

USBCAMD calls the camera minidriver's <b>CamNewVideoFrameEx</b> callback function at IRQL = DISPATCH_LEVEL.

The original USBCAMD does not call <b>CamNewVideoFrameEx</b>.

This function is optional.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | usbcamdi.h (include Usbcamdi.h) |
| **Library** |  |
| **IRQL** | DISPATCH_LEVEL (See Remarks section) |
| **DDI compliance rules** |  |