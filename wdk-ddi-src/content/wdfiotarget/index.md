---
UID : NA:wdfiotarget
ms.assetid : 65c859a2-b54e-397f-a79a-3c718b10f60c
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# wdfiotarget.h header



wdfiotarget.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [EVT_WDF_IO_TARGET_QUERY_REMOVE](nc-wdfiotarget-evt_wdf_io_target_query_remove.md) | A driver's EvtIoTargetQueryRemove event callback function indicates whether the framework can safely remove a specified remote I/O target's device. |
| [EVT_WDF_IO_TARGET_REMOVE_CANCELED](nc-wdfiotarget-evt_wdf_io_target_remove_canceled.md) | A driver's EvtIoTargetRemoveCanceled event callback function performs operations when the removal of a specified remote I/O target is canceled. |
| [EVT_WDF_IO_TARGET_REMOVE_COMPLETE](nc-wdfiotarget-evt_wdf_io_target_remove_complete.md) | A driver's EvtIoTargetRemoveComplete event callback function performs operations when the removal of a specified remote I/O target is complete. |
| [WDF_IO_TARGET_OPEN_PARAMS_INIT_CREATE_BY_NAME](nf-wdfiotarget-wdf_io_target_open_params_init_create_by_name.md) | The WDF_IO_TARGET_OPEN_PARAMS_INIT_CREATE_BY_NAME function initializes a driver's WDF_IO_TARGET_OPEN_PARAMS structure so the driver can open an I/O target by specifying the name of the device, file, or device interface. |
| [WDF_IO_TARGET_OPEN_PARAMS_INIT_EXISTING_DEVICE](nf-wdfiotarget-wdf_io_target_open_params_init_existing_device.md) | The WDF_IO_TARGET_OPEN_PARAMS_INIT_EXISTING_DEVICE function initializes a driver's WDF_IO_TARGET_OPEN_PARAMS structure so that the driver can open a remote I/O target by specifying a Windows Driver Model (WDM) device object. |
| [WDF_IO_TARGET_OPEN_PARAMS_INIT_OPEN_BY_FILE](nf-wdfiotarget-wdf_io_target_open_params_init_open_by_file.md) | The WDF_IO_TARGET_OPEN_PARAMS_INIT_OPEN_BY_FILE function initializes a driver's WDF_IO_TARGET_OPEN_PARAMS structure so the driver can open an I/O target by specifying a filename. |
| [WDF_IO_TARGET_OPEN_PARAMS_INIT_OPEN_BY_NAME](nf-wdfiotarget-wdf_io_target_open_params_init_open_by_name.md) | The WDF_IO_TARGET_OPEN_PARAMS_INIT_OPEN_BY_NAME function initializes a driver's WDF_IO_TARGET_OPEN_PARAMS structure so the driver can open an I/O target by specifying the name of the device, file, or device interface. |
| [WDF_IO_TARGET_OPEN_PARAMS_INIT_REOPEN](nf-wdfiotarget-wdf_io_target_open_params_init_reopen.md) | The WDF_IO_TARGET_OPEN_PARAMS_INIT_REOPEN function initializes a driver's WDF_IO_TARGET_OPEN_PARAMS structure so the driver can reopen a remote I/O target. |
| [WdfIoTargetAllocAndQueryTargetProperty](nf-wdfiotarget-wdfiotargetallocandquerytargetproperty.md) | The WdfIoTargetAllocAndQueryTargetProperty method allocates a buffer and retrieves a specified device property for a specified I/O target. |
| [WdfIoTargetClose](nf-wdfiotarget-wdfiotargetclose.md) | The WdfIoTargetClose method closes a specified remote I/O target. |
| [WdfIoTargetCloseForQueryRemove](nf-wdfiotarget-wdfiotargetcloseforqueryremove.md) | The WdfIoTargetCloseForQueryRemove method temporarily closes a specified remote I/O target because the target device might soon be removed. |
| [WdfIoTargetCreate](nf-wdfiotarget-wdfiotargetcreate.md) | The WdfIoTargetCreate method creates a remote I/O target for a specified device. |
| [WdfIoTargetFormatRequestForInternalIoctl](nf-wdfiotarget-wdfiotargetformatrequestforinternalioctl.md) | The WdfIoTargetFormatRequestForInternalIoctl method builds an internal device control request for an I/O target but does not send the request. |
| [WdfIoTargetFormatRequestForInternalIoctlOthers](nf-wdfiotarget-wdfiotargetformatrequestforinternalioctlothers.md) | The WdfIoTargetFormatRequestForInternalIoctlOthers method builds a non-standard internal device control request for an I/O target but does not send the request. |
| [WdfIoTargetFormatRequestForIoctl](nf-wdfiotarget-wdfiotargetformatrequestforioctl.md) | The WdfIoTargetFormatRequestForIoctl method builds a device control request for an I/O target but does not send the request. |
| [WdfIoTargetFormatRequestForRead](nf-wdfiotarget-wdfiotargetformatrequestforread.md) | The WdfIoTargetFormatRequestForRead method builds a read request for an I/O target but does not send the request. |
| [WdfIoTargetFormatRequestForWrite](nf-wdfiotarget-wdfiotargetformatrequestforwrite.md) | The WdfIoTargetFormatRequestForWrite method builds a write request for an I/O target but does not send the request. |
| [WdfIoTargetGetDevice](nf-wdfiotarget-wdfiotargetgetdevice.md) | The WdfIoTargetGetDevice method returns a handle to the framework device object that is the parent of the specified local or remote I/O target. |
| [WdfIoTargetGetState](nf-wdfiotarget-wdfiotargetgetstate.md) | The WdfIoTargetGetState method returns state information for a local or remote I/O target. |
| [WdfIoTargetOpen](nf-wdfiotarget-wdfiotargetopen.md) | The WdfIoTargetOpen method opens a remote I/O target so the driver can send I/O requests to it. |
| [WdfIoTargetPurge](nf-wdfiotarget-wdfiotargetpurge.md) | The WdfIoTargetPurge method cancels all I/O requests queued to a local, remote, or specialized I/O target and prevents any new I/O requests from being queued. |
| [WdfIoTargetQueryForInterface](nf-wdfiotarget-wdfiotargetqueryforinterface.md) | The WdfIoTargetQueryForInterface method obtains access to the GUID-identified, driver-defined interface of a remote I/O target. |
| [WdfIoTargetQueryTargetProperty](nf-wdfiotarget-wdfiotargetquerytargetproperty.md) | The WdfIoTargetQueryTargetProperty method retrieves a specified device property for a specified I/O target. |
| [WdfIoTargetSendInternalIoctlOthersSynchronously](nf-wdfiotarget-wdfiotargetsendinternalioctlotherssynchronously.md) | The WdfIoTargetSendInternalIoctlOthersSynchronously method builds a non-standard internal device control request and sends it synchronously to an I/O target. |
| [WdfIoTargetSendInternalIoctlSynchronously](nf-wdfiotarget-wdfiotargetsendinternalioctlsynchronously.md) | The WdfIoTargetSendInternalIoctlSynchronously method builds an internal device control request and sends it synchronously to an I/O target. |
| [WdfIoTargetSendIoctlSynchronously](nf-wdfiotarget-wdfiotargetsendioctlsynchronously.md) | The WdfIoTargetSendIoctlSynchronously method builds a device control request and sends it synchronously to an I/O target. |
| [WdfIoTargetSendReadSynchronously](nf-wdfiotarget-wdfiotargetsendreadsynchronously.md) | The WdfIoTargetSendReadSynchronously method builds a read request and sends it synchronously to an I/O target. |
| [WdfIoTargetSendWriteSynchronously](nf-wdfiotarget-wdfiotargetsendwritesynchronously.md) | The WdfIoTargetSendWriteSynchronously method builds a write request and sends it synchronously to an I/O target. |
| [WdfIoTargetStart](nf-wdfiotarget-wdfiotargetstart.md) | The WdfIoTargetStart method starts sending queued requests to a local or remote I/O target. |
| [WdfIoTargetStop](nf-wdfiotarget-wdfiotargetstop.md) | The WdfIoTargetStop method stops sending queued requests to a local or remote I/O target. |
| [WdfIoTargetWdmGetTargetDeviceObject](nf-wdfiotarget-wdfiotargetwdmgettargetdeviceobject.md) | The WdfIoTargetWdmGetTargetDeviceObject method returns a pointer to the Windows Driver Model (WDM) device object that is associated with a specified local or remote I/O target. |
| [WdfIoTargetWdmGetTargetFileHandle](nf-wdfiotarget-wdfiotargetwdmgettargetfilehandle.md) | The WdfIoTargetWdmGetTargetFileHandle method returns a handle to the file that is associated with a specified remote I/O target. |
| [WdfIoTargetWdmGetTargetFileObject](nf-wdfiotarget-wdfiotargetwdmgettargetfileobject.md) | The WdfIoTargetWdmGetTargetFileObject method returns a pointer to the Windows Driver Model (WDM) file object that is associated with a specified remote I/O target. |
| [WdfIoTargetWdmGetTargetPhysicalDevice](nf-wdfiotarget-wdfiotargetwdmgettargetphysicaldevice.md) | The WdfIoTargetWdmGetTargetPhysicalDevice method returns a pointer to the Windows Driver Model (WDM) physical device object (PDO) that represents a remote I/O target's device. |



## Structures
| Title | Description |
| ---- |:---- |
| [_WDF_IO_TARGET_OPEN_PARAMS](ns-wdfiotarget-_wdf_io_target_open_params.md) | The WDF_IO_TARGET_OPEN_PARAMS structure contains parameters that the WdfIoTargetOpen method uses. |


## Enumerations
| Title | Description |
| ---- |:---- |
| [_WDF_IO_TARGET_OPEN_TYPE](ne-wdfiotarget-_wdf_io_target_open_type.md) | The WDF_IO_TARGET_OPEN_TYPE enumeration specifies how a driver identifies a remote I/O target when the driver calls WdfIoTargetOpen. |
| [_WDF_IO_TARGET_PURGE_IO_ACTION](ne-wdfiotarget-_wdf_io_target_purge_io_action.md) | The WDF_IO_TARGET_PURGE_IO_ACTION enumeration identifies the actions that the framework can take when a driver calls WdfIoTargetPurge to purge an I/O target. |
| [_WDF_IO_TARGET_SENT_IO_ACTION](ne-wdfiotarget-_wdf_io_target_sent_io_action.md) | The WDF_IO_TARGET_SENT_IO_ACTION enumeration identifies the actions that the framework can take when a driver calls WdfIoTargetStop to stop an I/O target. |
| [_WDF_IO_TARGET_STATE](ne-wdfiotarget-_wdf_io_target_state.md) | The WDF_IO_TARGET_STATE enumeration specifies the states that an I/O target can be in. |