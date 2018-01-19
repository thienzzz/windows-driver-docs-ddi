---
UID : NC:usbbusif.USBC_START_DEVICE_CALLBACK
title : USBC_START_DEVICE_CALLBACK
author : windows-driver-content
description : The USBC_START_DEVICE_CALLBACK routine allows a USB client driver to provide a custom definition of the interface collections on a device.
old-location : buses\usbc_start_device_callback.htm
old-project : usbref
ms.assetid : f9a9510a-b55c-4566-83ce-4ed7ccafb543
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _USBD_VERSION_INFORMATION, *PUSBD_VERSION_INFORMATION, USBD_VERSION_INFORMATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : usbbusif.h
req.include-header : Usbbusif.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : UsbcStartDeviceCallback
req.alt-loc : usbbusif.h
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
req.typenames : "*PUSBD_VERSION_INFORMATION, USBD_VERSION_INFORMATION"
req.product : Windows 10 or later.
---


# USBC_START_DEVICE_CALLBACK callback function
The <b>USBC_START_DEVICE_CALLBACK</b> routine allows a USB client driver to provide a custom definition of the interface collections on a device.

## Syntax

```
USBC_START_DEVICE_CALLBACK UsbcStartDeviceCallback;

NTSTATUS UsbcStartDeviceCallback(
  PUSB_DEVICE_DESCRIPTOR DeviceDescriptor,
  PUSB_CONFIGURATION_DESCRIPTOR ConfigurationDescriptor,
  PUSBC_FUNCTION_DESCRIPTOR *FunctionDescriptorBuffer,
  PULONG FunctionDescriptorBufferLength,
  PDEVICE_OBJECT FdoDeviceObject,
  PDEVICE_OBJECT PdoDeviceObject
)
{...}
```

## Parameters

`DeviceDescriptor`

The device descriptor of the device.

`ConfigurationDescriptor`

The configuration of the device.

`*FunctionDescriptorBuffer`



`FunctionDescriptorBufferLength`

The length in bytes of the buffer that <i>FunctionDescriptorBuffer</i> points to.

`FdoDeviceObject`

The function device object for the device.

`PdoDeviceObject`

The physical device object for the device.


## Return Value

If the operation succeeds, the vendor-supplied callback routine must return STATUS_SUCCESS.

## Remarks

For a general description of the callback routine mechanism, see <a href="https://msdn.microsoft.com/3cf4e9f2-ea33-491f-94af-62d2afacc899">Customizing Enumeration of Interface Collections for Composite Devices</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | usbbusif.h (include Usbbusif.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\usbbusif\ns-usbbusif-_usbc_device_configuration_interface_v1.md">USBC_DEVICE_CONFIGURATION_INTERFACE_V1</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20USBC_START_DEVICE_CALLBACK callback function%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>