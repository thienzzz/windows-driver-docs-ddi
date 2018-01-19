---
UID : NE:hdaudio._HDAUDIO_STREAM_STATE
title : _HDAUDIO_STREAM_STATE
author : windows-driver-content
description : The HDAUDIO_STREAM_STATE enumeration defines constants that specify the different stream states supported by HDAudio.
old-location : audio\hdaudio_stream_state.htm
old-project : audio
ms.assetid : A1029A2D-980F-44F5-B7D6-1C37F97D0368
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _HDAUDIO_STREAM_STATE, HDAUDIO_STREAM_STATE, *PHDAUDIO_STREAM_STATE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : hdaudio.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : HDAUDIO_STREAM_STATE
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
req.irql : PASSIVE_LEVEL.
req.typenames : HDAUDIO_STREAM_STATE, *PHDAUDIO_STREAM_STATE
---

# _HDAUDIO_STREAM_STATE Enumeration
The <b>HDAUDIO_STREAM_STATE</b> enumeration defines constants that specify the different stream states supported by HDAudio.

## Syntax
````
typedef enum _HDAUDIO_STREAM_STATE { 
  ResetState  = 0,
  StopState   = 1,
  PauseState  = 1,
  RunState    = 2
} HDAUDIO_STREAM_STATE, *PHDAUDIO_STREAM_STATE;
````

## Constants

<table>

<tr>
<td>PauseState</td>
<td>The pause state.</td>
</tr>

<tr>
<td>ResetState</td>
<td>The reset state.</td>
</tr>

<tr>
<td>RunState</td>
<td>The run state.</td>
</tr>

<tr>
<td>StopState</td>
<td>The stop state.</td>
</tr>
</table>

## Remarks

This enumeration is used by the <a href="..\hdaudio\nc-hdaudio-pset_dma_engine_state.md">PSET_DMA_ENGINE_STATE</a>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hdaudio.h |