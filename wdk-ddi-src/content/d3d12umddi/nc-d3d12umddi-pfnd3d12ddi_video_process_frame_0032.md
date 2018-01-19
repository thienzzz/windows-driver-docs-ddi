---
UID : NC:d3d12umddi.PFND3D12DDI_VIDEO_PROCESS_FRAME_0032
title : PFND3D12DDI_VIDEO_PROCESS_FRAME_0032
author : windows-driver-content
description : Used to process a video frame.
old-location : display\pfnd3d12ddi_video_process_frame_0032.htm
old-project : display
ms.assetid : C7923B09-FBA2-43EE-A56B-0B8B6C3403A0
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3D11_1DDI_GETCAPTUREHANDLEDATA, D3D11_1DDI_GETCAPTUREHANDLEDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d12umddi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PFND3D12DDI_VIDEO_PROCESS_FRAME_0032
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


# PFND3D12DDI_VIDEO_PROCESS_FRAME_0032 callback function
Used to process a video frame.

## Syntax

```
PFND3D12DDI_VIDEO_PROCESS_FRAME_0032 Pfnd3d12ddiVideoProcessFrame0032;

void Pfnd3d12ddiVideoProcessFrame0032(
  D3D12DDI_HCOMMANDLIST hDrvCommandList,
  D3D12DDI_HVIDEOPROCESSOR_0020 hDrvVideoProcessor,
  const D3D12DDIARG_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS_0032 *pOutputParameters,
  const D3D12DDIARG_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS_0032 *pInputStreamParameters,
  UINT NumInputStreams
)
{...}
```

## Parameters

`hDrvCommandList`

The command list.

`hDrvVideoProcessor`

The video processor.

`*pOutputParameters`



`*pInputStreamParameters`



`NumInputStreams`

The number of input streams.


## Return Value

This callback function does not return a value.


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