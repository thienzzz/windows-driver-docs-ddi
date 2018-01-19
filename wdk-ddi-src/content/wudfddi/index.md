---
UID : NA:wudfddi
ms.assetid : 745c454f-313d-357e-8fd6-1042c8d6f353
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# wudfddi.h header



wudfddi.h contains the following programming interfaces:



## Interfaces
| Title | Description |
| ---- |:---- |
| [IDriverEntry](nn-wudfddi-idriverentry.md) | The IDriverEntry interface exposes the user-mode driver's main entry and exit points. |
| [IFileCallbackCleanup](nn-wudfddi-ifilecallbackcleanup.md) | The framework can notify a driver when the driver should perform a cleanup operation. |
| [IFileCallbackClose](nn-wudfddi-ifilecallbackclose.md) | The framework can notify a driver when the driver should perform a close operation. The driver can handle the notification by registering the IFileCallbackClose interface. |
| [IImpersonateCallback](nn-wudfddi-iimpersonatecallback.md) | The IImpersonateCallback interface contains a method that handles impersonation. |
| [IObjectCleanup](nn-wudfddi-iobjectcleanup.md) | Any driver that stores a reference-counted COM interface to a WDF object must support the IObjectCleanup interface to prevent interface leakage. Note that drivers, in general, are not required to hold references to WDF objects. |
| [IPnpCallback](nn-wudfddi-ipnpcallback.md) | The IPnpCallback interface is a Plug and Play (PnP) and power management (PM) interface. |
| [IPnpCallbackHardware](nn-wudfddi-ipnpcallbackhardware.md) | The IPnpCallbackHardware interface is a Plug and Play (PnP) and power management (PM) interface. |
| [IPnpCallbackHardware2](nn-wudfddi-ipnpcallbackhardware2.md) | The IPnpCallbackHardware2 interface exposes callback methods related to hardware. |
| [IPnpCallbackHardwareInterrupt](nn-wudfddi-ipnpcallbackhardwareinterrupt.md) | The IPnpCallbackHardwareInterrupt interface supports interrupt-related Plug and Play and power management callback methods. |
| [IPnpCallbackRemoteInterfaceNotification](nn-wudfddi-ipnpcallbackremoteinterfacenotification.md) | A driver's IPnpCallbackRemoteInterfaceNotification interface provides a callback function that the framework calls to notify the driver when a device interface becomes available. |
| [IPnpCallbackSelfManagedIo](nn-wudfddi-ipnpcallbackselfmanagedio.md) | The IPnpCallbackSelfManagedIo interface is a Plug and Play (PnP) and power management (PM) interface. |
| [IPowerPolicyCallbackWakeFromS0](nn-wudfddi-ipowerpolicycallbackwakefroms0.md) | A driver's IPowerPolicyCallbackWakeFromS0 interface provides callback functions that the framework calls to notify the driver about wake events. |
| [IPowerPolicyCallbackWakeFromSx](nn-wudfddi-ipowerpolicycallbackwakefromsx.md) | A driver's IPowerPolicyCallbackWakeFromSx interface provides callback functions that the framework calls to notify the driver about wake events. These events are related to a device's ability to wake both itself and the system from a low-power state. |
| [IQueueCallbackCreate](nn-wudfddi-iqueuecallbackcreate.md) | An I/O queue notifies a driver when an open file request is available for the driver. |
| [IQueueCallbackDefaultIoHandler](nn-wudfddi-iqueuecallbackdefaultiohandler.md) | The IQueueCallbackDefaultIoHandler interface contains a method that handles I/O requests that no other method is registered to handle. |
| [IQueueCallbackDeviceIoControl](nn-wudfddi-iqueuecallbackdeviceiocontrol.md) | An I/O queue object notifies a driver when a device I/O control request is available for the driver. |
| [IQueueCallbackIoCanceledOnQueue](nn-wudfddi-iqueuecallbackiocanceledonqueue.md) | The IQueueCallbackIoCanceledOnQueue interface is optional. Your driver can provide this interface if you want UMDF to notify the driver when an I/O request is canceled while it is in the driver's I/O queue. |
| [IQueueCallbackIoResume](nn-wudfddi-iqueuecallbackioresume.md) | The IQueueCallbackIoResume interface contains a method that resumes the processing of an I/O request from a queue. |
| [IQueueCallbackIoStop](nn-wudfddi-iqueuecallbackiostop.md) | The IQueueCallbackIoStop interface contains a method that stops the processing of an I/O request from a queue. |
| [IQueueCallbackRead](nn-wudfddi-iqueuecallbackread.md) | An I/O queue notifies a driver when a read request is available for the driver. |
| [IQueueCallbackStateChange](nn-wudfddi-iqueuecallbackstatechange.md) | An I/O queue object raises an event when it changes state. A driver can consume the event by registering the IQueueCallbackStateChange interface. |
| [IQueueCallbackWrite](nn-wudfddi-iqueuecallbackwrite.md) | An I/O queue object notifies a driver when a write request is available for the driver. |
| [IRemoteInterfaceCallbackEvent](nn-wudfddi-iremoteinterfacecallbackevent.md) | The IRemoteInterfaceCallbackEvent interface provides a callback function that the framework calls to notify the driver about device events that are associated with a device interface. |
| [IRemoteInterfaceCallbackRemoval](nn-wudfddi-iremoteinterfacecallbackremoval.md) | The IRemoteInterfaceCallbackRemoval provides a callback function that the framework calls to notify the driver about the removal of a device interface. |
| [IRemoteTargetCallbackRemoval](nn-wudfddi-iremotetargetcallbackremoval.md) | The IRemoteTargetCallbackRemoval interface provides callback functions that the framework calls to notify the driver about events that are associated with the removal of a remote I/O target. |
| [IRequestCallbackCancel](nn-wudfddi-irequestcallbackcancel.md) | A driver is notified when an I/O request that the driver is currently processing is to be canceled. |
| [IRequestCallbackRequestCompletion](nn-wudfddi-irequestcallbackrequestcompletion.md) | A driver implements the IRequestCallbackRequestCompletion interface to complete a request object. |
| [IWDFCmResourceList](nn-wudfddi-iwdfcmresourcelist.md) | This interface represents a list of hardware resources for a device. |
| [IWDFDevice](nn-wudfddi-iwdfdevice.md) | The IWDFDevice interface exposes a device object, which is a representation of a device on the system. |
| [IWDFDevice2](nn-wudfddi-iwdfdevice2.md) | Drivers obtain the IWDFDevice2 interface by calling IWDFDevice::QueryInterface. |
| [IWDFDevice3](nn-wudfddi-iwdfdevice3.md) | To obtain the IWDFDevice3 interface, drivers call IWDFDevice::QueryInterface. |
| [IWDFDeviceInitialize](nn-wudfddi-iwdfdeviceinitialize.md) | The IWDFDeviceInitialize interface is a helper interface that the framework supplies as an input parameter to the driver's IDriverEntry::OnDeviceAdd method. |
| [IWDFDeviceInitialize2](nn-wudfddi-iwdfdeviceinitialize2.md) | The IWDFDeviceInitialize2 interface is a helper interface that allows a driver to specify a preferred buffer retrieval mode and buffer access method. |
| [IWDFDriver](nn-wudfddi-iwdfdriver.md) | The IWDFDriver interface exposes the framework driver object that represents the driver image that is loaded in the host process. |
| [IWDFDriverCreatedFile](nn-wudfddi-iwdfdrivercreatedfile.md) | The IWDFDriverCreatedFile interface exposes a UMDF driver-created-file object for the driver to use. |
| [IWDFFile](nn-wudfddi-iwdffile.md) | The IWDFFile interface exposes the file object that represents the HANDLE that is returned by the Microsoft Win32 CreateFile function. |
| [IWDFFile2](nn-wudfddi-iwdffile2.md) | Drivers obtain the IWDFFile2 interface by calling IWDFFile::QueryInterface. |
| [IWDFFile3](nn-wudfddi-iwdffile3.md) | Drivers obtain the IWDFFile3 interface by calling IWDFFile::QueryInterface. |
| [IWDFFileHandleTargetFactory](nn-wudfddi-iwdffilehandletargetfactory.md) | The IWDFFileHandleTargetFactory interface is a factory interface that is used to create a file-handle-based target device object. |
| [IWDFInterrupt](nn-wudfddi-iwdfinterrupt.md) | This interface exposes an interrupt object. |
| [IWDFIoQueue](nn-wudfddi-iwdfioqueue.md) | The IWDFIoQueue interface exposes an I/O queue object. |
| [IWDFIoRequest](nn-wudfddi-iwdfiorequest.md) | The IWDFIoRequest interface exposes an I/O request object. |
| [IWDFIoRequest2](nn-wudfddi-iwdfiorequest2.md) | To obtain the IWDFIoRequest2 interface, drivers call IWDFIoRequest::QueryInterface. |
| [IWDFIoRequest3](nn-wudfddi-iwdfiorequest3.md) | To obtain the IWDFIoRequest3 interface, drivers call IWDFIoRequest::QueryInterface. |
| [IWDFIoRequestCompletionParams](nn-wudfddi-iwdfiorequestcompletionparams.md) | The IWDFIoRequestCompletionParams interface exposes methods that drivers can use to obtain completion information about an I/O request. Drivers can call these methods after a synchronous or asynchronous I/O operation completes. |
| [IWDFIoTarget](nn-wudfddi-iwdfiotarget.md) | The IWDFIoTarget interface exposes the I/O target object that typically represents a lower driver in the stack. |
| [IWDFIoTarget2](nn-wudfddi-iwdfiotarget2.md) | To obtain the IWDFIoTarget2 interface, drivers call IWDFIoTarget::QueryInterface. |
| [IWDFIoTargetStateManagement](nn-wudfddi-iwdfiotargetstatemanagement.md) | The IWDFIoTargetStateManagement interface exposes methods that manage and monitor the state of an I/O target object. |
| [IWDFMemory](nn-wudfddi-iwdfmemory.md) | The IWDFMemory interface exposes the framework memory object that provides access to a memory block. |
| [IWDFNamedPropertyStore](nn-wudfddi-iwdfnamedpropertystore.md) | The IWDFNamedPropertyStore interface exposes a property-store object. |
| [IWDFNamedPropertyStore2](nn-wudfddi-iwdfnamedpropertystore2.md) | Drivers obtain the IWDFNamedPropertyStore2 interface by calling IWDFPropertyStoreFactory::RetrieveDevicePropertyStore. |
| [IWDFObject](nn-wudfddi-iwdfobject.md) | The IWDFObject interface exposes the framework base object that provides the basic functionality common across all framework object types. All framework objects are derived from this root object. |
| [IWDFPropertyStoreFactory](nn-wudfddi-iwdfpropertystorefactory.md) | The IWDFPropertyStoreFactory interface is a factory interface that is used to create a property store interface. |
| [IWDFRemoteInterface](nn-wudfddi-iwdfremoteinterface.md) | UMDF drivers receive a pointer to this interface by calling the IWDFDevice2::CreateRemoteInterface method. |
| [IWDFRemoteInterfaceInitialize](nn-wudfddi-iwdfremoteinterfaceinitialize.md) | UMDF-based drivers receive the IWDFRemoteInterfaceInitialize interface as input to an IPnpCallbackRemoteInterfaceNotification::OnRemoteInterfaceArrival callback function. |
| [IWDFRemoteTarget](nn-wudfddi-iwdfremotetarget.md) | To obtain the IWDFRemoteTarget interface, drivers call IWDFDevice2::CreateRemoteTarget. |
| [IWDFRequestCompletionParams](nn-wudfddi-iwdfrequestcompletionparams.md) | The IWDFRequestCompletionParams interface exposes methods that drivers can use to obtain completion information about an I/O request. Drivers can call these methods after a synchronous or an asynchronous I/O operation completes. |
| [IWDFUnifiedPropertyStore](nn-wudfddi-iwdfunifiedpropertystore.md) | The IWDFUnifiedPropertyStore interface exposes a unified property store. |
| [IWDFUnifiedPropertyStoreFactory](nn-wudfddi-iwdfunifiedpropertystorefactory.md) | The IWDFUnifiedPropertyStoreFactory interface is a factory interface that is used to create a unified property store interface. |
| [IWDFWorkItem](nn-wudfddi-iwdfworkitem.md) | This interface exposes a work item object. |





## Structures
| Title | Description |
| ---- |:---- |
| [_UMDF_IO_TARGET_OPEN_PARAMS](ns-wudfddi-_umdf_io_target_open_params.md) | The UMDF_IO_TARGET_OPEN_PARAMS structure contains file-open parameters. |


## Enumerations
| Title | Description |
| ---- |:---- |
| [__MIDL___MIDL_itf_wudfddi_0000_0000_0001](ne-wudfddi-__midl___midl_itf_wudfddi_0000_0000_0001.md) | The POWER_ACTION enumeration identifies the system power actions that can occur on a computer. |
| [_DEVICE_POWER_STATE](ne-wudfddi-_device_power_state.md) | The DEVICE_POWER_STATE enumeration identifies the device power states that a device can enter. |
| [_SECURITY_IMPERSONATION_LEVEL](ne-wudfddi-_security_impersonation_level.md) | The SECURITY_IMPERSONATION_LEVEL enumeration contains values that identify security impersonation levels. |