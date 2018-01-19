---
UID : NI:ucmtcpciportcontrollerrequests.IOCTL_UCMTCPCI_PORT_CONTROLLER_SET_CONTROL
title : IOCTL_UCMTCPCI_PORT_CONTROLLER_SET_CONTROL
author : windows-driver-content
description : Sets the value of a control register defined as per the Universal Serial Bus Type-C Port Controller Interface Specification.
old-location : buses\ioctl_ucmtcpci_port_controller_set_control.htm
old-project : usbref
ms.assetid : F37BFBBE-B175-40AE-BE34-A4D6B00735D0
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _UCMTCPCI_PORT_CONTROLLER_IOCTL, UCMTCPCI_PORT_CONTROLLER_IOCTL
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : ucmtcpciportcontrollerrequests.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IOCTL_UCMTCPCI_PORT_CONTROLLER_SET_CONTROL
req.alt-loc : UcmTcpciPortControllerRequests.h
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
req.typenames : UCMTCPCI_PORT_CONTROLLER_IOCTL
req.product : Windows 10 or later.
---

# IOCTL_UCMTCPCI_PORT_CONTROLLER_SET_CONTROL IOCTL
Sets the value of a control register defined as per the Universal Serial Bus Type-C Port Controller Interface Specification.

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer
A pointer to a <a href="..\ucmtcpciportcontrollerrequests\ns-ucmtcpciportcontrollerrequests-_ucmtcpci_port_controller_set_control_in_params.md">UCMTCPCI_PORT_CONTROLLER_SET_CONTROL_IN_PARAMS</a> structure that contains the type of register and the value to set.

### Input Buffer Length
The size of the <a href="..\ucmtcpciportcontrollerrequests\ns-ucmtcpciportcontrollerrequests-_ucmtcpci_port_controller_set_control_in_params.md">UCMTCPCI_PORT_CONTROLLER_SET_CONTROL_IN_PARAMS</a> structure.

### Output Buffer
<text></text>

### Output Buffer Length
<text></text>

### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
I/O Status block
<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code.

    ## Remarks
        The UcmTcpciCx class extension sends this IOCTL request to set values to the control register. Only one register can be set per request. The type and value to set is provided in the supplied structure. After setting the value in the register, client driver must call <a href="..\wdfrequest\nf-wdfrequest-wdfrequestcomplete.md">WdfRequestComplete</a> to complete the request.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | ucmtcpciportcontrollerrequests.h |
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
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20IOCTL_UCMTCPCI_PORT_CONTROLLER_SET_CONTROL control code%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>