---
UID : NA:usbbusif
ms.assetid : ef304279-d2bf-341c-bda2-c51a3077b4a4
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# usbbusif.h header



usbbusif.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [USBC_START_DEVICE_CALLBACK](nc-usbbusif-usbc_start_device_callback.md) | The USBC_START_DEVICE_CALLBACK routine allows a USB client driver to provide a custom definition of the interface collections on a device. |



## Structures
| Title | Description |
| ---- |:---- |
| [_USB_BUS_INFORMATION_LEVEL_0](ns-usbbusif-_usb_bus_information_level_0.md) | The USB_BUS_INFORMATION_LEVEL_0 structure is used in conjunction with the QueryBusInformation interface routine to report information about the bus. |
| [_USB_BUS_INFORMATION_LEVEL_1](ns-usbbusif-_usb_bus_information_level_1.md) | The USB_BUS_INFORMATION_LEVEL_1 structure is used in conjunction with the QueryBusInformation interface routine to report information about the bus. |
| [_USB_BUS_INTERFACE_USBDI_V0](ns-usbbusif-_usb_bus_interface_usbdi_v0.md) | The USB_BUS_INTERFACE_USBDI_V0 structure is provided by the USB hub driver to allow USB clients to make direct calls to the hub driver without allocating IRPs. |
| [_USB_BUS_INTERFACE_USBDI_V1](ns-usbbusif-_usb_bus_interface_usbdi_v1.md) | The USB_BUS_INTERFACE_USBDI_V1 structure is provided by the USB hub driver to allow USB clients to make direct calls to the hub driver without allocating IRPs. |
| [_USB_BUS_INTERFACE_USBDI_V2](ns-usbbusif-_usb_bus_interface_usbdi_v2.md) | The USB_BUS_INTERFACE_USBDI_V2 structure is provided by the USB hub driver to allow USB clients to make direct calls to the hub driver without allocating IRPs. |
| [_USB_BUS_INTERFACE_USBDI_V3](ns-usbbusif-_usb_bus_interface_usbdi_v3.md) | The USB_BUS_INTERFACE_USBDI_V3 structure is provided by the USB hub driver to allow USB clients to make direct calls to the hub driver without allocating IRPs. |
| [_USBC_DEVICE_CONFIGURATION_INTERFACE_V1](ns-usbbusif-_usbc_device_configuration_interface_v1.md) | The USBC_DEVICE_CONFIGURATION_INTERFACE_V1 structure is exposed by the vendor-supplied filter drivers to assist the USB generic parent driver in defining interface collections. |
| [_USBC_FUNCTION_DESCRIPTOR](ns-usbbusif-_usbc_function_descriptor.md) | The USBC_FUNCTION_DESCRIPTOR structure describes a USB function and its associated interface collection. |