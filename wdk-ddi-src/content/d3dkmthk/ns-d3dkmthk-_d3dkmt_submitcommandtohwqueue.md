---
UID : NS:d3dkmthk._D3DKMT_SUBMITCOMMANDTOHWQUEUE
title : _D3DKMT_SUBMITCOMMANDTOHWQUEUE
author : windows-driver-content
description : A structure that holds information to submit a command to the hardware queue.
old-location : display\d3dkmt_submitcommandtohwqueue.htm
old-project : display
ms.assetid : 3807BD27-FAE4-4E12-A825-A9FAFB7A6ACA
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_SUBMITCOMMANDTOHWQUEUE, D3DKMT_SUBMITCOMMANDTOHWQUEUE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmthk.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMT_SUBMITCOMMANDTOHWQUEUE
req.alt-loc : d3dkmthk.h
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
req.typenames : D3DKMT_SUBMITCOMMANDTOHWQUEUE
---

# _D3DKMT_SUBMITCOMMANDTOHWQUEUE structure
A structure that holds information to submit a command to the hardware queue.

## Syntax
````
typedef struct _D3DKMT_SUBMITCOMMANDTOHWQUEUE {
  D3DKMT_HANDLE          hHwQueue;
  UINT64                 HwQueueProgressFenceId;
  D3DGPU_VIRTUAL_ADDRESS  CommandBuffer;
  UINT                   CommandLength;
  UINT                   PrivateDriverDataSize;
  VOID                   *pPrivateDriverData;
  UINT                   NumPrimaries;
  D3DKMT_HANDLE CONST    *WrittenPrimaries;
} D3DKMT_SUBMITCOMMANDTOHWQUEUE;
````

## Members

        
            `CommandLength`

            Length in bytes of the command buffer.
        
            `hHwQueue`

            Context queue to submit the command to.
        
            `HwQueueProgressFenceId`

            Hardware queue progress fence value that will be signaled once the command is finished.
        
            `NumPrimaries`

            The number of primaries written by this command buffer.
        
            `pPrivateDriverData`

            Pointer to the private driver data.
        
            `PrivateDriverDataSize`

            Size of private driver data in bytes.
        
            `WrittenPrimaries`

            The array of primaries written by this command buffer.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h |