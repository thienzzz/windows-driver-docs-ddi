---
UID : NS:wdfusb._WDF_USB_CONTROL_SETUP_PACKET
title : _WDF_USB_CONTROL_SETUP_PACKET
author : windows-driver-content
description : The WDF_USB_CONTROL_SETUP_PACKET structure describes a setup packet for a USB control transfer.
old-location : wdf\wdf_usb_control_setup_packet.htm
old-project : wdf
ms.assetid : f50ee559-3df7-4e15-b5a6-d6b85277c461
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDF_USB_CONTROL_SETUP_PACKET, *PWDF_USB_CONTROL_SETUP_PACKET, WDF_USB_CONTROL_SETUP_PACKET
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : wdfusb.h
req.include-header : Wdfusb.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 2.0
req.alt-api : WDF_USB_CONTROL_SETUP_PACKET
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
req.typenames : "*PWDF_USB_CONTROL_SETUP_PACKET, WDF_USB_CONTROL_SETUP_PACKET"
req.product : Windows 10 or later.
---

# _WDF_USB_CONTROL_SETUP_PACKET structure
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_USB_CONTROL_SETUP_PACKET</b> structure describes a setup packet for a USB control transfer.

## Syntax
````
typedef union _WDF_USB_CONTROL_SETUP_PACKET {
  struct {
    union {
      struct {
        BYTE Recipient  :2;
        BYTE Reserved  :3;
        BYTE Type  :2;
        BYTE Dir  :1;
      } Request;
      BYTE   Byte;
    } bm;
    BYTE   bRequest;
    union {
      struct {
        BYTE LowByte;
        BYTE HiByte;
      } Bytes;
      USHORT Value;
    } wValue;
    union {
      struct {
        BYTE LowByte;
        BYTE HiByte;
      } Bytes;
      USHORT Value;
    } wIndex;
    USHORT wLength;
  } Packet;
  struct {
    BYTE Bytes[8];
  } Generic;
} WDF_USB_CONTROL_SETUP_PACKET, *PWDF_USB_CONTROL_SETUP_PACKET;
````

## Members

        
            `Generic`

            
        
            `Packet`

            

    ## Remarks
        The <b>WDF_USB_CONTROL_SETUP_PACKET</b> structure is used as input to the <a href="..\wdfusb\nf-wdfusb-wdfusbtargetdevicesendcontroltransfersynchronously.md">WdfUsbTargetDeviceSendControlTransferSynchronously</a> and <a href="..\wdfusb\nf-wdfusb-wdfusbtargetdeviceformatrequestforcontroltransfer.md">WdfUsbTargetDeviceFormatRequestForControlTransfer</a> methods.

To initialize a <b>WDF_USB_CONTROL_SETUP_PACKET</b> structure, the driver should call one of the following functions:


<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init.md">WDF_USB_CONTROL_SETUP_PACKET_INIT</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_class.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_CLASS</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_feature.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_FEATURE</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_get_status.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_GET_STATUS</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_control_setup_packet_init_vendor.md">WDF_USB_CONTROL_SETUP_PACKET_INIT_VENDOR</a>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfusb.h (include Wdfusb.h) |

    ## See Also

        <dl>
<dt>
<a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_direction.md">WDF_USB_BMREQUEST_DIRECTION</a>
</dt>
<dt>
<a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_recipient.md">WDF_USB_BMREQUEST_RECIPIENT</a>
</dt>
<dt>
<a href="..\wdfusb\ne-wdfusb-_wdf_usb_bmrequest_type.md">WDF_USB_BMREQUEST_TYPE</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdfusbtargetdeviceformatrequestforcontroltransfer.md">WdfUsbTargetDeviceFormatRequestForControlTransfer</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdfusbtargetdevicesendcontroltransfersynchronously.md">WdfUsbTargetDeviceSendControlTransferSynchronously</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_USB_CONTROL_SETUP_PACKET union%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>