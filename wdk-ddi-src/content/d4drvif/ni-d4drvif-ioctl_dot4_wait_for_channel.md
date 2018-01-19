---
UID : NI:d4drvif.IOCTL_DOT4_WAIT_FOR_CHANNEL
title : IOCTL_DOT4_WAIT_FOR_CHANNEL
author : windows-driver-content
description : This topic describes IOCTL_DOT4_WAIT_FOR_CHANNEL.
old-location : print\ioctl_ioctl_dot4_wait_for_channel.htm
old-project : print
ms.assetid : 4FFC0BE7-A095-4229-A713-566815B53EAF
ms.author : windowsdriverdev
ms.date : 1/8/2018
ms.keywords : _GETENCRYPTIONBLTKEY, D3DDDIARG_GETENCRYPTIONBLTKEY
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : d4drvif.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IOCTL_DOT4_WAIT_FOR_CHANNEL
req.alt-loc : D4drvif.h
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
req.typenames : D3DDDIARG_GETENCRYPTIONBLTKEY
---

# IOCTL_DOT4_WAIT_FOR_CHANNEL IOCTL
This topic describes <b>IOCTL_DOT4_WAIT_FOR_CHANNEL</b>.

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer


### Input Buffer Length
None

### Output Buffer


### Output Buffer Length


### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
I/O Status block
<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | d4drvif.h |
| **IRQL** |  |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff542894">Creating IOCTL Requests in Drivers</a>
</dt>
<dt>
<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendinternalioctlotherssynchronously.md">WdfIoTargetSendInternalIoctlOthersSynchronously</a>
</dt>
<dt>
<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendinternalioctlsynchronously.md">WdfIoTargetSendInternalIoctlSynchronously</a>
</dt>
<dt>
<a href="..\wdfiotarget\nf-wdfiotarget-wdfiotargetsendioctlsynchronously.md">WdfIoTargetSendIoctlSynchronously</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IOCTL_DOT4_WAIT_FOR_CHANNEL control code%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>