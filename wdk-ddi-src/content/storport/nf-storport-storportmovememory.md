---
UID : NF:storport.StorPortMoveMemory
title : StorPortMoveMemory function
author : windows-driver-content
description : The StorPortMoveMemory routine copies memory from one buffer to another.
old-location : storage\storportmovememory.htm
old-project : storage
ms.assetid : 5481ae5e-c28a-478e-96be-c6ec8d7f163e
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortMoveMemory
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortMoveMemory
req.alt-loc : Storport.lib,Storport.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Storport.lib
req.dll : 
req.irql : 
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortMoveMemory function
The <b>StorPortMoveMemory</b> routine copies memory from one buffer to another.

## Syntax

````
STORPORT_API VOID StorPortMoveMemory(
  _In_ PVOID WriteBuffer,
  _In_ PVOID ReadBuffer,
  _In_ ULONG Length
);
````

## Parameters

`WriteBuffer`

Pointer to the destination buffer.

`ReadBuffer`

Pointer to the source buffer.

`Length`

Specifies how many bytes to transfer from <i>ReadBuffer</i> to <i>WriteBuffer</i>.


## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\srb\nf-srb-scsiportmovememory.md">ScsiPortMoveMemory</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortMoveMemory routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>