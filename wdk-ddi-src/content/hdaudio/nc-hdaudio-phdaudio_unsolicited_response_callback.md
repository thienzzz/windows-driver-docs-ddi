---
UID : NC:hdaudio.PHDAUDIO_UNSOLICITED_RESPONSE_CALLBACK
title : PHDAUDIO_UNSOLICITED_RESPONSE_CALLBACK
author : windows-driver-content
description : HDAudio codec unsolicited response callback function. PHDAUDIO_UNSOLICITED_RESPONSE_CALLBACK is used by the PREGISTER_EVENT_CALLBACK callback function.
old-location : audio\phdaudio_unsolicited_response_callback.htm
old-project : audio
ms.assetid : B98F669D-D0DE-4FF2-903C-D51E0FEEE840
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
req.alt-api : HDAudioUnsolicitedResponseCallback
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


# PHDAUDIO_UNSOLICITED_RESPONSE_CALLBACK callback function
HDAudio codec unsolicited response callback function. <b>PHDAUDIO_UNSOLICITED_RESPONSE_CALLBACK</b> is used by the <a href="..\hdaudio\nc-hdaudio-pregister_event_callback.md">PREGISTER_EVENT_CALLBACK</a> callback function.

## Syntax

```
PHDAUDIO_UNSOLICITED_RESPONSE_CALLBACK PhdaudioUnsolicitedResponseCallback;

void PhdaudioUnsolicitedResponseCallback(
   HDAUDIO_CODEC_RESPONSE,
   PVOID
)
{...}
```

## Parameters

`HDAUDIO_CODEC_RESPONSE`



`PVOID`




## Return Value

Void

## Remarks

The HD Audio bus driver calls the callback routine at PASSIVE_LEVEL.</p>

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