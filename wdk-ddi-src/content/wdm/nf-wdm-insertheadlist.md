---
UID : NF:wdm.InsertHeadList
title : InsertHeadList function
author : windows-driver-content
description : The InsertHeadList routine inserts an entry at the head of a doubly linked list of LIST_ENTRY structures.
old-location : kernel\insertheadlist.htm
old-project : kernel
ms.assetid : c3ad9d93-93e1-406b-9a58-26dcbf428b50
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : InsertHeadList
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Desktop
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : InsertHeadList
req.alt-loc : Wdm.h
req.ddi-compliance : IoAllocateFree, IoReuseIrp, MarkingQueuedIrps, RemoveLockCheck, RemoveLockForward, RemoveLockForward2, RemoveLockForwardDeviceControl, RemoveLockForwardDeviceControl2, RemoveLockForwardDeviceControlInternal, RemoveLockForwardDeviceControlInternal2, RemoveLockForwardRead, RemoveLockForwardRead2, RemoveLockForwardWrite, RemoveLockForwardWrite2, RemoveLockRelease2, RemoveLockReleaseCleanup, RemoveLockReleaseClose, RemoveLockReleaseCreate, RemoveLockReleaseDeviceControl, RemoveLockReleaseInternalDeviceControl, RemoveLockReleasePower, RemoveLockReleaseRead, RemoveLockReleaseShutdown, RemoveLockReleaseSystemControl, RemoveLockReleaseWrite
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : Any level (See Remarks section)
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# InsertHeadList function
The <b>InsertHeadList</b> routine inserts an entry at the head of a doubly linked list of <a href="https://msdn.microsoft.com/library/windows/hardware/ff554296">LIST_ENTRY</a> structures.

## Syntax

````
VOID InsertHeadList(
  _Inout_ PLIST_ENTRY ListHead,
  _Inout_ PLIST_ENTRY Entry
);
````

## Parameters

`ListHead`

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554296">LIST_ENTRY</a> structure that represents the head of the list.

`Entry`

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff554296">LIST_ENTRY</a> structure that represents the entry to be inserted into the list.


## Return Value

None

## Remarks

<b>InsertHeadList</b> updates <i>ListHead</i>-&gt;<b>Flink</b> to point to <i>Entry</i>. It updates <i>Entry</i>-&gt;<b>Flink</b> to point to the old first entry in the list, and sets <i>Entry</i>-&gt;<b>Blink</b> to <i>ListHead</i>. The <b>Blink</b> field of the original first entry is also updated to point to <i>Entry</i>.

For information about using this routine when implementing a doubly linked list, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563802">Singly and Doubly Linked Lists</a>.

Callers of <b>InsertHeadList</b> can be running at any IRQL. If <b>InsertHeadList</b> is called at IRQL &gt;= DISPATCH_LEVEL, the storage for <i>ListHead</i> and the list entries must be resident.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | Any level (See Remarks section) |
| **DDI compliance rules** | IoAllocateFree, IoReuseIrp, MarkingQueuedIrps, RemoveLockCheck, RemoveLockForward, RemoveLockForward2, RemoveLockForwardDeviceControl, RemoveLockForwardDeviceControl2, RemoveLockForwardDeviceControlInternal, RemoveLockForwardDeviceControlInternal2, RemoveLockForwardRead, RemoveLockForwardRead2, RemoveLockForwardWrite, RemoveLockForwardWrite2, RemoveLockRelease2, RemoveLockReleaseCleanup, RemoveLockReleaseClose, RemoveLockReleaseCreate, RemoveLockReleaseDeviceControl, RemoveLockReleaseInternalDeviceControl, RemoveLockReleasePower, RemoveLockReleaseRead, RemoveLockReleaseShutdown, RemoveLockReleaseSystemControl, RemoveLockReleaseWrite |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-exinterlockedinsertheadlist.md">ExInterlockedInsertHeadList</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-initializelisthead.md">InitializeListHead</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-inserttaillist.md">InsertTailList</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-islistempty.md">IsListEmpty</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-removeheadlist.md">RemoveHeadList</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-removetaillist.md">RemoveTailList</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20InsertHeadList routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>