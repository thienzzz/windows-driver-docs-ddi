---
UID : NF:wdm.KeResetEvent
title : KeResetEvent function
author : windows-driver-content
description : The KeResetEvent routine resets a specified event object to a not-signaled state and returns the previous state of that event object.
old-location : kernel\keresetevent.htm
old-project : kernel
ms.assetid : 90be986b-e63e-4ae3-a0f3-87f6f58583dc
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : KeResetEvent
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KeResetEvent
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : IrqlKeDispatchLte, HwStorPortProhibitedDDIs
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : <=DISPATCH_LEVEL
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# KeResetEvent function
The <b>KeResetEvent</b> routine resets a specified event object to a not-signaled state and returns the previous state of that event object.

## Syntax

````
LONG KeResetEvent(
  _Inout_ PRKEVENT Event
);
````

## Parameters

`Event`

A pointer to an initialized dispatcher object of type event for which the caller provides the storage.


## Return Value

<b>KeResetEvent</b> returns a value that indicates the previous state of the specified <i>Event</i>, which is nonzero for a signaled state.

## Remarks

<i>Event</i> is reset to a not-signaled state, meaning that its value is set to zero.

Unless the caller requires the value that is returned by <b>KeResetEvent</b>, using the <a href="..\wdm\nf-wdm-keclearevent.md">KeClearEvent</a> routine is a faster way to set an event object to a not-signaled state.

For more information about event objects, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544323">Event Objects</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** | IrqlKeDispatchLte, HwStorPortProhibitedDDIs |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-keclearevent.md">KeClearEvent</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-keinitializeevent.md">KeInitializeEvent</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-kereadstateevent.md">KeReadStateEvent</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-kesetevent.md">KeSetEvent</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-kewaitformultipleobjects.md">KeWaitForMultipleObjects</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-kewaitforsingleobject.md">KeWaitForSingleObject</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20KeResetEvent routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>