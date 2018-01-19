---
UID : NA:hwnclx
ms.assetid : b41140bd-3a1f-3742-9971-e78555cd7456
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# hwnclx.h header



hwnclx.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [HWN_CLIENT_GET_STATE](nc-hwnclx-hwn_client_get_state.md) | Implemented by the client driver to get hardware notification component state. It is invoked when a user requests status information. |
| [HWN_CLIENT_INITIALIZE_DEVICE](nc-hwnclx-hwn_client_initialize_device.md) | Implemented by the client driver and is invoked as a result of a call to EVT_WDF_DEVICE_PREPARE_HARDWARE. |
| [HWN_CLIENT_QUERY_DEVICE_INFORMATION](nc-hwnclx-hwn_client_query_device_information.md) | Implemented by the client driver to retrieve hardware notification component attributes. |
| [HWN_CLIENT_SET_STATE](nc-hwnclx-hwn_client_set_state.md) | Implemented by the client driver to set hardware notification component state. It is invoked when a user wants to change the state of a driver. |
| [HWN_CLIENT_START_DEVICE](nc-hwnclx-hwn_client_start_device.md) | Implemented by the client driver to start the hardware notification component. It is invoked as a result of a call to EVT_WDF_DEVICE_D0_ENTRY. |
| [HWN_CLIENT_STOP_DEVICE](nc-hwnclx-hwn_client_stop_device.md) | Implemented by the client driver TO start the hardware notification component. It is invoked as a result of a call to EVT_WDF_DEVICE_D0_EXIT. |
| [HWN_CLIENT_UNINITIALIZE_DEVICE](nc-hwnclx-hwn_client_uninitialize_device.md) | Implemented by the client driver and invoked as invoked as a result of a call to EVT_WDF_DEVICE_RELEASE_HARDWARE. This callback function uninitializes the hardware notification component. |
| [HwNProcessAddDevicePostDeviceCreate](nf-hwnclx-hwnprocessadddevicepostdevicecreate.md) | Creates I/O queues. It should be called after the client driver’s EVT_WDF_DRIVER_DEVICE_ADD callback function is invoked and the device object has been created. |
| [HwNProcessAddDevicePreDeviceCreate](nf-hwnclx-hwnprocessadddevicepredevicecreate.md) | Supplies the device prepare/release and entry/exit callbacks to the Windows Driver Foundation (WDF) for transitioning the device into different states. |
| [HwNRegisterClient](nf-hwnclx-hwnregisterclient.md) | Registers the hardware notification client driver and its callback functions with the class extension. |
| [HwNUnregisterClient](nf-hwnclx-hwnunregisterclient.md) | Unregisters the hardware notification client driver and its callback functions with the class extension. This function should be invoked when the client driver is unloaded. |



## Structures
| Title | Description |
| ---- |:---- |
| [_CLIENT_DEVICE_INFORMATION](ns-hwnclx-_client_device_information.md) | The CLIENT_DEVICE_INFORMATION structure is used by the hardware notification callback HWN_CLIENT_QUERY_DEVICE_INFORMATION to return the total number of hardware notifications that the client device driver provides. |
| [_HWN_CLIENT_REGISTRATION_PACKET](ns-hwnclx-_hwn_client_registration_packet.md) | Hardware Notification client driver registration packet that is passed to the class extension when a client driver is registered. Contains version information and client driver callback functions. |


## Enumerations
| Title | Description |
| ---- |:---- |
| [_HWN_CLX_EXPORT_INDEX](ne-hwnclx-_hwn_clx_export_index.md) | Defines the position for each of the Hardware Notification exports in the export table. |