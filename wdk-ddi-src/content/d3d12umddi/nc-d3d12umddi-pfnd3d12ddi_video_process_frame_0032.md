---
UID: NC:d3d12umddi.PFND3D12DDI_VIDEO_PROCESS_FRAME_0032
title: PFND3D12DDI_VIDEO_PROCESS_FRAME_0032
author: windows-driver-content
description: Used to process a video frame.
old-location: display\pfnd3d12ddi_video_process_frame_0032.htm
old-project: display
ms.assetid: C7923B09-FBA2-43EE-A56B-0B8B6C3403A0
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: PFND3D12DDI_VIDEO_PROCESS_FRAME_0032, PFND3D12DDI_VIDEO_PROCESS_FRAME_0032 callback, PFND3D12DDI_VIDEO_PROCESS_FRAME_0032 callback function [Display Devices], d3d12umddi/PFND3D12DDI_VIDEO_PROCESS_FRAME_0032, display.pfnd3d12ddi_video_process_frame_0032
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3d12umddi.h
api_name:
-	PFND3D12DDI_VIDEO_PROCESS_FRAME_0032
product:
- Windows
targetos: Windows
req.typenames: 
---

# PFND3D12DDI_VIDEO_PROCESS_FRAME_0032 callback function


## -description


Used to process a video frame.


## -parameters




### -param hDrvCommandList

A handle to the driver's data for the command list. The driver uses this region of memory to store internal data structures that are related to its command list.


### -param hDrvVideoProcessor

The video processor.


### -param *pOutputParameters

The output arguments for the video process.


### -param *pInputStreamParameters

The input arguments for the video process.


### -param NumInputStreams

The number of input streams.


## -returns



This callback function does not return a value.



