---
UID : NF:video.VideoPortDebugPrint
title : VideoPortDebugPrint function
author : windows-driver-content
description : Video miniport drivers should not call the VideoPortDebugPrint function. Instead, they should call the VideoDebugPrint macro.
old-location : display\videoportdebugprint.htm
old-project : display
ms.assetid : c476c8a2-5d79-45cd-ae72-f8792137f9c2
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : VideoPortDebugPrint
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : video.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows XP and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : VideoPortDebugPrint
req.alt-loc : Videoprt.sys
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Videoprt.lib
req.dll : Videoprt.sys
req.irql : PASSIVE_LEVEL
req.typenames : VIDEO_PORT_SERVICES
req.product : Windows 10 or later.
---


# VideoPortDebugPrint function
Video miniport drivers should not call the <b>VideoPortDebugPrint</b> function. Instead, they should call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570170">VideoDebugPrint</a> macro.

## Syntax

````
VOID VideoPortDebugPrint(
       VIDEO_DEBUG_LEVEL DebugPrintLevel,
  _In_ PSTR              DebugMessage
);
````

## Parameters

`DebugPrintLevel`



`DebugMessage`

Pointer to a string that contains the debug message.

``




## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | video.h |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |