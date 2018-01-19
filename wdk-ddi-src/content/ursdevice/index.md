---
UID : NA:ursdevice
ms.assetid : 56f6c740-1ee6-329c-b645-7535d1122c7e
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# ursdevice.h header



ursdevice.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [EVT_URS_SET_ROLE](nc-ursdevice-evt_urs_set_role.md) | The URS class extension invokes this event callback when it requires the client driver to change the role of the controller. |
| [URS_CONFIG_INIT](nf-ursdevice-urs_config_init.md) | Initializes a URS_CONFIG structure. |
| [UrsDeviceInitialize](nf-ursdevice-ursdeviceinitialize.md) | Initializes a framework device object to support operations related to a USB dual-role controller and registers the relevant event callback functions with the USB dual-role controller class extension. |
| [UrsDeviceInitInitialize](nf-ursdevice-ursdeviceinitinitialize.md) | Initializes device initialization operations when the Plug and Play (PnP) manager reports the existence of a device. |
| [UrsIoResourceListAppendDescriptor](nf-ursdevice-ursioresourcelistappenddescriptor.md) | Appends the specified resource descriptor to the specified I/O resource list object that maintains resource descriptors for the host or function role. |
| [UrsReportHardwareEvent](nf-ursdevice-ursreporthardwareevent.md) | Notifies the USB dual-role class extension about a new hardware event. |
| [UrsSetHardwareEventSupport](nf-ursdevice-urssethardwareeventsupport.md) | Indicates the client driver's support for reporting new hardware events. |
| [UrsSetPoHandle](nf-ursdevice-urssetpohandle.md) | Registers and deletes the client driver's registration with the power management framework (PoFx). |



## Structures
| Title | Description |
| ---- |:---- |
| [_URS_CONFIG](ns-ursdevice-_urs_config.md) | Contains pointers to event callback functions implemented by the URS client driver for a USB dual-role controller. Initialize this structure by calling URS_CONFIG_INIT. |