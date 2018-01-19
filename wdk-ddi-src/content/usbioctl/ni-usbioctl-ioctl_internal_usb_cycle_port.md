---
UID : NI:usbioctl.IOCTL_INTERNAL_USB_CYCLE_PORT
title : IOCTL_INTERNAL_USB_CYCLE_PORT
author : windows-driver-content
description : The IOCTL_INTERNAL_USB_CYCLE_PORT I/O request simulates a device unplug and replug on the port associated with the PDO.
old-location : buses\ioctl_internal_usb_cycle_port.htm
old-project : usbref
ms.assetid : 81e62377-66af-4588-8be5-f6bb89a11fe0
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _USB_HUB_TYPE, USB_HUB_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : usbioctl.h
req.include-header : Usbioctl.h
req.target-type : Windows
req.target-min-winverclnt : Windows XP and later operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IOCTL_INTERNAL_USB_CYCLE_PORT
req.alt-loc : Usbioctl.h
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
req.typenames : USB_HUB_TYPE
req.product : Windows 10 or later.
---

# IOCTL_INTERNAL_USB_CYCLE_PORT IOCTL
The <b>IOCTL_INTERNAL_USB_CYCLE_PORT</b> I/O request simulates a device unplug and replug on the port associated with the PDO. 

Drivers should cancel all I/O requests and wait for them to complete before initiating this operation. 

A driver that manages an individual interface on a composite device cannot cycle the port to which the device is attached without affecting the entire composite device and all of its interfaces. For this reason, drivers that manage interfaces should attempt other types of error recovery, such as resetting pipes (<a href="..\usb\ns-usb-_urb_pipe_request.md">_URB_PIPE_REQUEST</a>), before cycling the port. 

<b>IOCTL_INTERNAL_USB_CYCLE_PORT</b> is a kernel-mode I/O control request. This request targets the USB hub PDO. This request must be sent at an IRQL of PASSIVE_LEVEL.



The <b>IOCTL_INTERNAL_USB_CYCLE_PORT</b> I/O request simulates a device unplug and replug on the port associated with the PDO. 

Drivers should cancel all I/O requests and wait for them to complete before initiating this operation. 

A driver that manages an individual interface on a composite device cannot cycle the port to which the device is attached without affecting the entire composite device and all of its interfaces. For this reason, drivers that manage interfaces should attempt other types of error recovery, such as resetting pipes (<a href="..\usb\ns-usb-_urb_pipe_request.md">_URB_PIPE_REQUEST</a>), before cycling the port. 

<b>IOCTL_INTERNAL_USB_CYCLE_PORT</b> is a kernel-mode I/O control request. This request targets the USB hub PDO. This request must be sent at an IRQL of PASSIVE_LEVEL.

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer
None.

### Input Buffer Length
None.

### Output Buffer
None.

### Output Buffer Length
None.

### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
I/O Status block
The bus or port driver sets <b>Irp-&gt;IoStatus.Status</b> to STATUS_SUCCESS or the appropriate error status.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | usbioctl.h (include Usbioctl.h) |
| **IRQL** |  |