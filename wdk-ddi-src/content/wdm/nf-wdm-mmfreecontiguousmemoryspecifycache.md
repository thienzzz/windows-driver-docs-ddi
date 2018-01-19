---
UID : NF:wdm.MmFreeContiguousMemorySpecifyCache
title : MmFreeContiguousMemorySpecifyCache function
author : windows-driver-content
description : The MmFreeContiguousMemorySpecifyCache routine frees a buffer that was allocated by an MmAllocateContiguousMemorySpecifyCacheXxx routine.
old-location : kernel\mmfreecontiguousmemoryspecifycache.htm
old-project : kernel
ms.assetid : e5958dd7-b287-4f0d-8677-75d850885262
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : MmFreeContiguousMemorySpecifyCache
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : MmFreeContiguousMemorySpecifyCache
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : <= DISPATCH_LEVEL
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# MmFreeContiguousMemorySpecifyCache function
The <b>MmFreeContiguousMemorySpecifyCache</b> routine frees a buffer that was allocated by an <b>MmAllocateContiguousMemorySpecifyCache<i>Xxx</i></b> routine.

## Syntax

````
VOID MmFreeContiguousMemorySpecifyCache(
  _In_ PVOID               BaseAddress,
  _In_ SIZE_T              NumberOfBytes,
  _In_ MEMORY_CACHING_TYPE CacheType
);
````

## Parameters

`BaseAddress`

Specifies the base address of the buffer to be freed. Must match the address returned by the <b>MmAllocateContiguousMemorySpecifyCache<i>Xxx</i></b> call that allocated the buffer.

`NumberOfBytes`

Specifies the size in bytes of the buffer to be freed. Must match the size requested when the buffer was allocated by the <b>MmAllocateContiguousMemorySpecifyCache<i>Xxx</i></b> routine.

`CacheType`

Specifies the cache type of the buffer to be freed. Must match the cache type requested when the buffer was allocated by the <b>MmAllocateContiguousMemorySpecifyCache<i>Xxx</i></b> routine.


## Return Value

None

## Remarks

The <b>MmFreeContiguousMemorySpecifyCache</b> routine frees a block of physically contiguous memory that was allocated by a previous call to the <a href="..\wdm\nf-wdm-mmallocatecontiguousmemoryspecifycache.md">MmAllocateContiguousMemorySpecifyCache</a> or <a href="..\wdm\nf-wdm-mmallocatecontiguousmemoryspecifycachenode.md">MmAllocateContiguousMemorySpecifyCacheNode</a> routine. However, <a href="..\wdm\nf-wdm-mmfreecontiguousmemory.md">MmFreeContiguousMemory</a> is the preferred routine to use to free memory that was allocated by an <b>MmAllocateContiguousMemorySpecifyCache<i>Xxx</i></b> routine. <b>MmFreeContiguousMemory</b> is faster than <b>MmFreeContiguousMemorySpecifyCache</b> and requires fewer parameters.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-mmallocatecontiguousmemoryspecifycache.md">MmAllocateContiguousMemorySpecifyCache</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-mmallocatecontiguousmemoryspecifycachenode.md">MmAllocateContiguousMemorySpecifyCacheNode</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-mmfreecontiguousmemory.md">MmFreeContiguousMemory</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20MmFreeContiguousMemorySpecifyCache routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>