---
UID : NF:usbdlib.UsbBuildGetStatusRequest
title : UsbBuildGetStatusRequest macro
author : windows-driver-content
description : The UsbBuildGetStatusRequest macro formats an URB to obtain status from a device, interface, endpoint, or other device-defined target on a USB device.
old-location : buses\usbbuildgetstatusrequest.htm
old-project : usbref
ms.assetid : 7a5fcb4f-fc9a-4ebb-93ef-b83461557b22
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : UsbBuildGetStatusRequest
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : macro
req.header : usbdlib.h
req.include-header : Usbdlib.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : UsbBuildGetStatusRequest
req.alt-loc : usbdlib.h
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
req.typenames : USBCAMD_DEVICE_DATA2, *PUSBCAMD_DEVICE_DATA2
req.product : Windows 10 or later.
---


# UsbBuildGetStatusRequest function
The <b>UsbBuildGetStatusRequest</b> macro formats an <a href="..\usb\ns-usb-_urb.md">URB</a> to obtain status from a device, interface, endpoint, or other device-defined target on a USB device.

## Syntax

````
void UsbBuildGetStatusRequest(
  _Inout_         Urb,
  _In_     USHORT Op,
  _In_     USHORT Index,
  _In_opt_ PVOID  TransferBuffer,
  _In_opt_ PMDL   TransferBufferMDL,
  _In_     PURB   Link
);
````

## Parameters

`urb`



`op`



`index`



`transferBuffer`



`transferBufferMDL`



`link`




## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | usbdlib.h (include Usbdlib.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\usb\ns-usb-_urb.md">URB</a>
</dt>
<dt>
<a href="..\usb\ns-usb-_urb_control_get_status_request.md">_URB_CONTROL_GET_STATUS_REQUEST</a>
</dt>
<dt><a href="usb_reference.htm#client">USB device driver programming reference</a></dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UsbBuildGetStatusRequest routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>