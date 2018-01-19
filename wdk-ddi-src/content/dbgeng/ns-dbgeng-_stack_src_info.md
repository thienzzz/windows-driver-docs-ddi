---
UID : NS:dbgeng._STACK_SRC_INFO
title : _STACK_SRC_INFO
author : windows-driver-content
description : Defines stack source information.
old-location : debugger\stack_src_info.htm
old-project : debugger
ms.assetid : F19D5A5C-D9CF-40CC-B344-8F2D862FBF04
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _STACK_SRC_INFO, *PSTACK_SRC_INFO, STACK_SRC_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : STACK_SRC_INFO
req.alt-loc : dbgeng.h
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
req.typenames : "*PSTACK_SRC_INFO, STACK_SRC_INFO"
---

# _STACK_SRC_INFO structure
Defines stack source information.

## Syntax
````
typedef struct _STACK_SRC_INFO {
  PCWSTR ImagePath;
  PCWSTR ModuleName;
  PCWSTR Function;
  ULONG  Displacement;
  ULONG  Row;
  ULONG  Column;
} STACK_SRC_INFO, *PSTACK_SRC_INFO;
````

## Members

        
            `Column`

            A column number.
        
            `Displacement`

            A displacement value.
        
            `Function`

            A function.
        
            `ImagePath`

            An image path.
        
            `ModuleName`

            A module name.
        
            `Row`

            A row number.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |