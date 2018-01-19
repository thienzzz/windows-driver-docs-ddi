---
UID : NF:ndis.NdisInterlockedIncrement
title : NdisInterlockedIncrement macro
author : windows-driver-content
description : The NdisInterlockedIncrement function increments a caller-supplied variable as an atomic operation.
old-location : netvista\ndisinterlockedincrement.htm
old-project : netvista
ms.assetid : 246ded7a-4f75-469d-bdba-860ce3cd6b44
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisInterlockedIncrement
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : macro
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Universal
req.target-min-winverclnt : Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisInterlockedIncrement (NDIS   5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see    NdisInterlockedIncrement (NDIS   5.1)) in Windows XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisInterlockedIncrement
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ndis.lib
req.dll : 
req.irql : Any level
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisInterlockedIncrement function
The 
  <b>NdisInterlockedIncrement</b> function increments a caller-supplied variable as an atomic
  operation.

## Syntax

````
LONG NdisInterlockedIncrement(
  [in] PLONG Addend
);
````

## Parameters

`Addend`

A pointer to a variable of type LONG.


## Return Value

None

## Remarks

<b>NdisInterlockedIncrement</b> cannot be used on variables in pageable memory.

<b>NdisInterlockedIncrement</b> is atomic only with respect to other 
    <b>NdisInterlocked<i>Xxx</i></b> calls.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |
| **Library** |  |
| **IRQL** | Any level |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ndis\nf-ndis-ndisinterlockeddecrement.md">NdisInterlockedDecrement</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisInterlockedIncrement macro%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>