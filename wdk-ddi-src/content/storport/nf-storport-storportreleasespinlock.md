---
UID : NF:storport.StorPortReleaseSpinLock
title : StorPortReleaseSpinLock function
author : windows-driver-content
description : The StorPortReleaseSpinLock routine releases a spinlock acquired by StorPortAcquireSpinLock.
old-location : storage\storportreleasespinlock.htm
old-project : storage
ms.assetid : ed91d41a-575d-4b26-a7e0-f3ce43db76b4
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortReleaseSpinLock
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
req.alt-api : StorPortReleaseSpinLock
req.alt-loc : storport.h
req.ddi-compliance : StorPortSpinLock, StorPortSpinLock4
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortReleaseSpinLock function
The <b>StorPortReleaseSpinLock</b> routine releases a spinlock acquired by <a href="..\storport\nf-storport-storportacquirespinlock.md">StorPortAcquireSpinLock</a>.

## Syntax

````
VOID StorPortReleaseSpinLock(
  _In_    PVOID             HwDeviceExtension,
  _Inout_ PSTOR_LOCK_HANDLE LockHandle
);
````

## Parameters

`DeviceExtension`



`LockHandle`

Pointer to a lock handle returned by <a href="..\storport\nf-storport-storportacquirespinlock.md">StorPortAcquireSpinLock</a>.


## Return Value

None.


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
| **DDI compliance rules** | StorPortSpinLock, StorPortSpinLock4 |

## See Also

<dl>
<dt>
<a href="..\storport\nf-storport-storportacquirespinlock.md">StorPortAcquireSpinLock</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortReleaseSpinLock routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>