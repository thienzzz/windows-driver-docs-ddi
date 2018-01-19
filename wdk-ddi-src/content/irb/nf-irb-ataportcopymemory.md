---
UID : NF:irb.AtaPortCopyMemory
title : AtaPortCopyMemory function
author : windows-driver-content
description : The AtaPortCopyMemory routine copies data from one location to another.Note  The ATA port driver and ATA miniport driver models may be altered or unavailable in the future.
old-location : storage\ataportcopymemory.htm
old-project : storage
ms.assetid : f5e449f8-9ff9-4d3d-9a62-3e985b57bd50
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : AtaPortCopyMemory
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : irb.h
req.include-header : Ata.h, Irb.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : AtaPortCopyMemory
req.alt-loc : ataport.lib,ataport.dll,pciidex.lib,pciidex.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ataport.lib; Pciidex.lib
req.dll : 
req.irql : 
req.typenames : IDE_POWER_STATE
---


# AtaPortCopyMemory function
The <b>AtaPortCopyMemory</b> routine copies data from one location to another.

## Syntax

````
VOID AtaPortCopyMemory(
  _Out_ PVOID WriteBuffer,
  _In_  PVOID ReadBuffer,
  _In_  ULONG Length
);
````

## Parameters

`WriteBuffer`

A pointer to the destination buffer.

`ReadBuffer`

A pointer to the source buffer.

`Length`

Specifies the number of bytes to transfer from <i>ReadBuffer</i> to <i>WriteBuffer</i>.


## Return Value

None

## Remarks

The miniport driver calls the <b>AtaPortCopy</b><b>Memory</b> routine to copy data from one system-allocated area to another.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | irb.h (include Ata.h, Irb.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |