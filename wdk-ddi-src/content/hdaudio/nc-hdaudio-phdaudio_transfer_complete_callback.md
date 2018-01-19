---
UID : NC:hdaudio.PHDAUDIO_TRANSFER_COMPLETE_CALLBACK
title : PHDAUDIO_TRANSFER_COMPLETE_CALLBACK
author : windows-driver-content
description : HDAudio codec transfer complete callback function. PHDAUDIO_TRANSFER_COMPLETE_CALLBACK is used by the PTRANSFER_CODEC_VERBS callback function.
old-location : audio\phdaudio_transfer_complete_callback.htm
old-project : audio
ms.assetid : 6B3DA3B1-33E9-4BE4-A3EE-146080C483A6
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _SM_SetRNIDMgmtInfo_OUT, SM_SetRNIDMgmtInfo_OUT, *PSM_SetRNIDMgmtInfo_OUT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : hdaudio.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : HDAudioTransferCompleteCallback
req.alt-loc : Hdaudio.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : SM_SetRNIDMgmtInfo_OUT, *PSM_SetRNIDMgmtInfo_OUT
---


# PHDAUDIO_TRANSFER_COMPLETE_CALLBACK callback function
HDAudio codec transfer complete callback function. <b>PHDAUDIO_TRANSFER_COMPLETE_CALLBACK</b> is used by the <a href="..\hdaudio\nc-hdaudio-ptransfer_codec_verbs.md">PTRANSFER_CODEC_VERBS</a> callback function.

## Syntax

```
PHDAUDIO_TRANSFER_COMPLETE_CALLBACK PhdaudioTransferCompleteCallback;

void PhdaudioTransferCompleteCallback(
  HDAUDIO_CODEC_TRANSFER *,
   PVOID
)
{...}
```

## Parameters

`*`



`PVOID`




## Return Value

Void

## Remarks

For more information, see <a href="..\hdaudio\nc-hdaudio-ptransfer_codec_verbs.md">PTRANSFER_CODEC_VERBS</a>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hdaudio.h |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |