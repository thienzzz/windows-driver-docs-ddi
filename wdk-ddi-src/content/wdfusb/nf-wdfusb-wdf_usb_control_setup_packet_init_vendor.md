---
UID : NF:wdfusb.WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR
title : WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR function
author : windows-driver-content
description : The WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR function initializes a WDF_USB_CONTROL_SETUP_PACKET structure for a vendor-specific USB control transfer.
old-location : wdf\wdf_usb_control_setup_packet_init_vendor.htm
old-project : wdf
ms.assetid : 58774dcf-f48c-4d39-acbe-fe09b4c52d81
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfusb.h
req.include-header : Wdfusb.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 2.0
req.alt-api : WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR
req.alt-loc : wdfusb.h
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
req.typenames : "*PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE"
req.product : Windows 10 or later.
---


# WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR function
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR</b> function initializes a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure for a vendor-specific USB control transfer.

## Syntax

````
VOID WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR(
  _Out_ PWDF_USB_CONTROL_SETUP_PACKET Packet,
  _In_  WDF_USB_BMREQUEST_DIRECTION   Direction,
  _In_  WDF_USB_BMREQUEST_RECIPIENT   Recipient,
  _In_  BYTE                          Request,
  _In_  USHORT                        Value,
  _In_  USHORT                        Index
);
````

## Parameters

`Packet`

A pointer to a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

`Direction`

A <a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_direction.md">WDF_USB_BMREQUEST_DIRECTION</a>-typed value that is stored in the <b>Packet.bm.Request.Dir</b> member of the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

`Recipient`

A <a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_recipient.md">WDF_USB_BMREQUEST_RECIPIENT</a>-typed value that is stored in the <b>Packet.bm.Request.Recipient</b> member of the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

`Request`

A request type constant that is stored in the <b>Packet.bRequest</b> member of the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

`Value`

A request-specific value that is stored in the <b>Packet.wValue.Value</b> member of the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

`Index`

A request-specific index value that is stored in the <b>Packet.wIndex.Value</b> member of the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.


## Return Value

None

## Remarks

The <b>WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR</b> function does the following:

Zeros the <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

Sets the <b>Packet.bm.Request.Type</b> member to <b>BmRequestVendor</b>.

Sets other structure members by using the <b>WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR</b> function's input arguments.

To initialize a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure, the driver should call one of the following functions:


<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init.md">WDF_USB_CONTROL_SETUP_PACKET_INIT</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_class.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_CLASS</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_feature.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_FEATURE</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_get_status.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_GET_STATUS</a>


<b>WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR</b>

The following code example initializes a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a> structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfusb.h (include Wdfusb.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_direction.md">WDF_USB_BMREQUEST_DIRECTION</a>
</dt>
<dt>
<a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_recipient.md">WDF_USB_BMREQUEST_RECIPIENT</a>
</dt>
<dt>
<a href="..\wdfusb\ns-wdfusb-_wdf_usb_control_setup_packet.md">WDF_USB_CONTROL_SETUP_PACKET</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init.md">WDF_USB_CONTROL_SETUP_PACKET_INIT</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_class.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_CLASS</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_feature.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_FEATURE</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_get_status.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_GET_STATUS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>