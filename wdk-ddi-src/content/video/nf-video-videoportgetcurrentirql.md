---
UID : NF:video.VideoPortGetCurrentIrql
title : VideoPortGetCurrentIrql function
author : windows-driver-content
description : The VideoPortGetCurrentIrql function gets the current IRQL.
old-location : display\videoportgetcurrentirql.htm
old-project : display
ms.assetid : 04cbc86b-a977-43bd-a736-3a7258c671fd
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : VideoPortGetCurrentIrql
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : video.h
req.include-header : Video.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : VideoPortGetCurrentIrql
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
req.irql : Any level
req.typenames : VIDEO_PORT_SERVICES
req.product : Windows 10 or later.
---


# VideoPortGetCurrentIrql function
The <b>VideoPortGetCurrentIrql</b> function gets the current IRQL.

## Syntax

````
UCHAR VideoPortGetCurrentIrql(void);
````

## Parameters

This function has no parameters.

## Return Value

<b>VideoPortGetCurrentIrql</b> returns the current IRQL.

<b>VideoPortGetCurrentIrql</b> returns the current IRQL.

<b>VideoPortGetCurrentIrql</b> returns the current IRQL.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | video.h (include Video.h) |
| **Library** |  |
| **IRQL** | Any level |
| **DDI compliance rules** |  |