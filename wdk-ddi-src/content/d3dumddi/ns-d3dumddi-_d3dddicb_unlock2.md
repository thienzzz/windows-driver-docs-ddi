---
UID : NS:d3dumddi._D3DDDICB_UNLOCK2
title : _D3DDDICB_UNLOCK2
author : windows-driver-content
description : D3DDDICB_UNLOCK2 describes an allocation to unlock.
old-location : display\d3dddicb_unlock2.htm
old-project : display
ms.assetid : 3ACE32ED-75C5-440D-BAA1-470C4E043299
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DDDICB_UNLOCK2, D3DDDICB_UNLOCK2
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DDDICB_UNLOCK2
req.alt-loc : d3dumddi.h
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
req.typenames : D3DDDICB_UNLOCK2
---

# _D3DDDICB_UNLOCK2 structure
<b>D3DDDICB_UNLOCK2</b> describes an allocation to unlock.

## Syntax
````
typedef struct _D3DDDICB_UNLOCK2 {
  D3DKMT_HANDLE hAllocation;
} D3DDDICB_UNLOCK2;
````

## Members

        
            `hAllocation`

            [in] A driver specified <b>D3DKMT_HANDLE</b> to the allocation to unlock.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |