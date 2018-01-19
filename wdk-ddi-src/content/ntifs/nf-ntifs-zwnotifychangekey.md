---
UID : NF:ntifs.ZwNotifyChangeKey
title : ZwNotifyChangeKey function
author : windows-driver-content
description : The ZwNotifyChangeKey routine allows a driver to request notification when a registry key changes.
old-location : kernel\zwnotifychangekey.htm
old-project : kernel
ms.assetid : 660c04b0-499b-40e7-94c2-5cb457e93f00
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : ZwNotifyChangeKey
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ZwNotifyChangeKey,NtNotifyChangeKey
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : PASSIVE_LEVEL
req.typenames : TOKEN_TYPE
---


# ZwNotifyChangeKey function
The <b>ZwNotifyChangeKey</b> routine allows a driver to request notification when a registry key changes.

## Syntax

````
NTSTATUS ZwNotifyChangeKey(
  _In_      HANDLE           KeyHandle,
  _In_opt_  HANDLE           Event,
  _In_opt_  PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_  PVOID            ApcContext,
  _Out_     PIO_STATUS_BLOCK IoStatusBlock,
  _In_      ULONG            CompletionFilter,
  _In_      BOOLEAN          WatchTree,
  _Out_opt_ PVOID            Buffer,
  _In_      ULONG            BufferSize,
  _In_      BOOLEAN          Asynchronous
);
````

## Parameters

`KeyHandle`

Handle to the key to register a notification routine for. This handle is created by a successful call to <a href="..\wdm\nf-wdm-zwcreatekey.md">ZwCreateKey</a> or <a href="..\wdm\nf-wdm-zwopenkey.md">ZwOpenKey</a>. The caller must have specified KEY_NOTIFY access.

`Event`

Handle to a caller-created event. If not <b>NULL</b>, the caller is placed into a wait state until the operation succeeds, at which time the event is set to the Signaled state.

`ApcRoutine`

For a user-mode call, this parameter points to a caller-supplied APC routine that is run after the operation is completed. This parameter is optional and can be <b>NULL</b>.

  For a kernel-mode call, this parameter must be <b>NULL</b>.

`ApcContext`

The meaning of this parameter depends on whether the routine is called from kernel mode or from user mode. For a kernel-mode call, set this parameter to one of the following <a href="..\wdm\ne-wdm-_work_queue_type.md">WORK_QUEUE_TYPE</a> enumeration values:

<ul>
<li>
CriticalWorkQueue

</li>
<li>
DelayedWorkQueue

</li>
</ul>
The parameter value must be cast to type PVOID. For a user-mode call, this parameter points to a caller-specified context for the APC routine. This value is passed to the APC routine when it is run.

`IoStatusBlock`

Pointer to an <a href="..\wdm\ns-wdm-_io_status_block.md">IO_STATUS_BLOCK</a> structure that contains the final status and information about the operation. For successful calls that return data, the number of bytes written to <i>Buffer</i> is supplied in <i>IoStatusBlock</i>-&gt;<b>Information</b>.

`CompletionFilter`

Bitmask of operations that cause the driver to be notified. Specify one or more of the following flags:

`WatchTree`

If <b>TRUE</b>, the driver is notified about changes to all subkeys of the specified key. If <b>FALSE</b>, the driver is only notified for changes to the specified key.

`Buffer`

Reserved. Specify <b>NULL</b>.

`BufferSize`

Reserved. Specify zero.

`Asynchronous`

If <b>FALSE</b>, the routine does not return until the specified event occurs. If <b>TRUE</b>, the routine returns immediately.


## Return Value

The <b>ZwNotifyChangeKey</b> routine returns STATUS_SUCCESS on success, or the appropriate NTSTATUS value otherwise. If the caller specifies <b>TRUE</b> for the <i>Asynchronous</i> parameter, and the event has not yet occurred, the routine returns STATUS_PENDING.

## Remarks

If the call to the <b>ZwNotifyChangeKey</b> function occurs in user mode, you should use the name "<b>NtNotifyChangeKey</b>" instead of "<b>ZwNotifyChangeKey</b>". 

For calls from kernel-mode drivers, the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a Windows Native System Services routine can behave differently in the way that they handle and interpret input parameters. For more information about the relationship between the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a routine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** | PowerIrpDDis, HwStorPortProhibitedDDIs |

## See Also

<dl>
<dt>
<a href="..\wdm\ns-wdm-_io_status_block.md">IO_STATUS_BLOCK</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwcreatekey.md">ZwCreateKey</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwopenkey.md">ZwOpenKey</a>
</dt>
<dt>
<a href="..\wdm\ns-wdm-_work_queue_item.md">WORK_QUEUE_ITEM</a>
</dt>
<dt>
<a href="..\wdm\ne-wdm-_work_queue_type.md">WORK_QUEUE_TYPE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ZwNotifyChangeKey routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>