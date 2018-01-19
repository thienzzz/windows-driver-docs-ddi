---
UID : NS:d3d12umddi.D3D12DDI_SWIZZLE_PATTERN_DESC_0022
title : D3D12DDI_SWIZZLE_PATTERN_DESC_0022
author : windows-driver-content
description : Describes a swizzle pattern.
old-location : display\d3d12ddi_swizzle_pattern_desc_0022.htm
old-project : display
ms.assetid : A52C8293-C037-4062-9A63-AD69237F7B3D
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D12DDI_SWIZZLE_PATTERN_DESC_0022, D3D12DDI_SWIZZLE_PATTERN_DESC_0022
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3d12umddi.h
req.include-header : D3d12umddi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D12DDI_SWIZZLE_PATTERN_DESC_0022
req.alt-loc : D3d12umddi.h
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
req.typenames : D3D12DDI_SWIZZLE_PATTERN_DESC_0022
---

# D3D12DDI_SWIZZLE_PATTERN_DESC_0022 structure
Describes a swizzle pattern.

## Syntax
````
typedef struct D3D12DDI_SWIZZLE_PATTERN_DESC_0022 {
  D3D12DDI_SWIZZLE_BIT_ENTRY InterleavePatternSourceBits[32];
  D3D12DDI_SWIZZLE_BIT_ENTRY InterleavePatternXORSourceBits[32];
  D3D12DDI_SWIZZLE_BIT_ENTRY InterleavePatternXOR2SourceBits[32];
  D3D12DDI_SWIZZLE_BIT_ENTRY InterleavePatternXOR3SourceBits[32];
  D3D12DDI_SWIZZLE_BIT_ENTRY InterleavePatternXOR4SourceBits[32];
  D3D12DDI_SWIZZLE_BIT_ENTRY PostambleXORSourceBits[32];
  D3D12DDI_SWIZZLE_BIT_ENTRY PostambleXOR2SourceBits[32];
  UINT                       PostambleXORImmediate;
  UINT                       Flags;
} D3D12DDI_SWIZZLE_PATTERN_DESC_0022;
````

## Members

        
            `Flags`

            Flags.
        
            `InterleavePatternSourceBits`

            The interleave pattern source bits.
        
            `InterleavePatternXOR2SourceBits`

            The interleave pattern second XOR source bits.
        
            `InterleavePatternXOR3SourceBits`

            The interleave pattern third XOR source bits.
        
            `InterleavePatternXOR4SourceBits`

            The interleave pattern fourth XOR source bits.
        
            `InterleavePatternXORSourceBits`

            The interleave pattern XOR source bits.
        
            `PostambleXOR2SourceBits`

            Postamble second XOR source bits.
        
            `PostambleXORImmediate`

            A postamble XOR immediate value.
        
            `PostambleXORSourceBits`

            Postamble XOR source bits.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d12umddi.h (include D3d12umddi.h) |