---
UID : NF:wdm.ObDereferenceObjectWithTag
title : ObDereferenceObjectWithTag macro
author : windows-driver-content
description : The ObDereferenceObjectWithTag routine decrements the reference count of the specified object, and writes a four-byte tag value to the object to support object reference tracing.
old-location : kernel\obdereferenceobjectwithtag.htm
old-project : kernel
ms.assetid : 872098c1-d684-4ce5-9f53-2fee8b50b626
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : ObDereferenceObjectWithTag
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : macro
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h, Fltkernel.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows 7 and later versions of the Windows operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ObDereferenceObjectWithTag
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : HwStorPortProhibitedDDIs
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


# ObDereferenceObjectWithTag function
The <b>ObDereferenceObjectWithTag</b> routine decrements the reference count of the specified object, and writes a four-byte tag value to the object to support <a href="http://go.microsoft.com/fwlink/p/?linkid=153590">object reference tracing</a>.

## Syntax

````
VOID ObDereferenceObjectWithTag(
  _In_ PVOID Object,
  _In_ ULONG Tag
);
````

## Parameters

`a`



`t`




## Return Value

None

## Remarks

A kernel-mode driver calls this routine to decrement the reference count of an object by one. If the object was created as <i>temporary</i> (that is, the OBJ_PERMANENT flag was not specified when the object was created), and the reference count reaches zero, the object manager deletes the object.

When the reference count for an object reaches zero, a kernel-mode component can delete the object. However, a driver can delete only those objects that it created, and a driver should never attempt to delete any object that it did not create.

An object is <i>permanent</i> if it was created with the OBJ_PERMANENT object attribute flag specified. (For more information about object attributes, see <a href="..\wudfwdm\nf-wudfwdm-initializeobjectattributes.md">InitializeObjectAttributes</a>.) A permanent object is created with an initial reference count of one, so the object is not deleted when the driver removes its last reference to the object.

To prepare a permanent object to be deleted, a driver can call the <a href="..\wdm\nf-wdm-zwmaketemporaryobject.md">ZwMakeTemporaryObject</a> routine to make the object temporary. A driver should only delete a permanent object that it created. Use the following steps to delete a permanent object:

Call <b>ObDereferenceObjectWithTag</b>. 

Get the handle to the object. If necessary, call the appropriate <b>ZwOpen<i>Xxx</i></b> or <b>ZwCreate<i>Xxx</i></b> routine to get the object handle.

Call <b>ZwMakeTemporaryObject</b> with the handle obtained in step 2. 

Call <a href="..\wdm\nf-wdm-zwclose.md">ZwClose</a> with the handle obtained in step 2.

If the immediate deletion of an object by the current thread might cause a deadlock, do not call <b>ObDereferenceObjectWithTag</b> to dereference the object. Instead, call the <a href="..\wdm\nf-wdm-obdereferenceobjectdeferdeletewithtag.md">ObDereferenceObjectDeferDeleteWithTag</a> routine to dereference the object.

For example, such a deadlock can occur if <b>ObDereferenceObjectWithTag</b> is used to dereference a <a href="https://msdn.microsoft.com/43bf96ed-8be8-4670-a310-99cd7c7f9073">Kernel Transaction Manager</a> (KTM) object when a higher-level driver on the driver stack is holding a lock.

For more information about object references, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff554294">Life Cycle of an Object</a>.

The <a href="..\wdm\nf-wdm-obdereferenceobject.md">ObDereferenceObject</a> routine is similar to <b>ObDereferenceObjectWithTag</b>, except that it does not enable the caller to write a custom tag to an object. In Windows 7 and later versions of Windows, <b>ObDereferenceObject</b> always writes a default tag value ('tlfD') to the object. A call to <b>ObDereferenceObject</b> has the same effect as a call to <b>ObDereferenceObjectWithTag</b> that specifies <i>Tag</i> = 'tlfD'.

To view an object reference trace in the <a href="http://go.microsoft.com/fwlink/p/?linkid=153599">Windows debugging tools</a>, use the <a href="http://go.microsoft.com/fwlink/p/?linkid=153600">!obtrace</a> kernel-mode debugger extension. In Windows 7, the <b>!obtrace</b> extension is enhanced to display object reference tags, if object reference tracing is enabled. By default, object reference tracing is turned off. Use the <a href="http://go.microsoft.com/fwlink/p/?linkid=153601">Global Flags Editor</a> (Gflags) to enable object reference tracing. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558668">Object Reference Tracing with Tags</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h, Fltkernel.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** | HwStorPortProhibitedDDIs |

## See Also

<dl>
<dt>
<a href="..\wudfwdm\nf-wudfwdm-initializeobjectattributes.md">InitializeObjectAttributes</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iogetdeviceobjectpointer.md">IoGetDeviceObjectPointer</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-obdereferenceobject.md">ObDereferenceObject</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-obdereferenceobjectdeferdeletewithtag.md">ObDereferenceObjectDeferDeleteWithTag</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-obreferenceobjectbyhandlewithtag.md">ObReferenceObjectByHandleWithTag</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwclose.md">ZwClose</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwmaketemporaryobject.md">ZwMakeTemporaryObject</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ObDereferenceObjectWithTag routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>