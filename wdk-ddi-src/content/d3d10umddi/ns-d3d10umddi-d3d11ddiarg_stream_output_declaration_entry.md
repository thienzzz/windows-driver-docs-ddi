---
UID : NS:d3d10umddi.D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY
title : D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY
author : windows-driver-content
description : The D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY structure describes a portion of the stream output for a geometry shader.
old-location : display\d3d11ddiarg_stream_output_declaration_entry.htm
old-project : display
ms.assetid : 336bfc9d-325b-4ff1-8d6b-ec2ef4158cb9
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY, D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY is supported beginning with the Windows 7 operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY
req.alt-loc : d3d10umddi.h
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
req.typenames : D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY
---

# D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY structure
The D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY structure describes a portion of the stream output for a geometry shader.

## Syntax
````
typedef struct D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY {
  UINT Stream;
  UINT OutputSlot;
  UINT RegisterIndex;
  BYTE RegisterMask;
} D3D11DDIARG_STREAM_OUTPUT_DECLARATION_ENTRY;
````

## Members

        
            `OutputSlot`

            [in] The number of the slot for the portion of the stream output.
        
            `RegisterIndex`

            [in] The number of the register for the portion of the stream output.
        
            `RegisterMask`

            [in] The xyzw register mask for the portion of the stream output. That is, the four least significant bits (LSBs) of the mask represent xyzw respectively.
        
            `Stream`

            [in] The stream to output from, which is a value between zero and the maximum number of streams that are specified by the driver.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |