---
UID : NS:wdfpdo._WDF_PDO_EVENT_CALLBACKS
title : _WDF_PDO_EVENT_CALLBACKS
author : windows-driver-content
description : The WDF_PDO_EVENT_CALLBACKS structure is the dispatch table for a bus driver's event callback functions.
old-location : wdf\wdf_pdo_event_callbacks.htm
old-project : wdf
ms.assetid : 13cb1da1-0bb7-444e-a0e1-abcac7d0240d
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDF_PDO_EVENT_CALLBACKS, WDF_PDO_EVENT_CALLBACKS, *PWDF_PDO_EVENT_CALLBACKS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : wdfpdo.h
req.include-header : Wdf.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 
req.alt-api : WDF_PDO_EVENT_CALLBACKS
req.alt-loc : wdfpdo.h
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
req.typenames : WDF_PDO_EVENT_CALLBACKS, *PWDF_PDO_EVENT_CALLBACKS
req.product : Windows 10 or later.
---

# _WDF_PDO_EVENT_CALLBACKS structure
<p class="CCE_Message">[Applies to KMDF only]

The <b>WDF_PDO_EVENT_CALLBACKS</b> structure is the dispatch table for a bus driver's event callback functions.

## Syntax
````
typedef struct _WDF_PDO_EVENT_CALLBACKS {
  ULONG                                      Size;
  PFN_WDF_DEVICE_RESOURCES_QUERY             EvtDeviceResourcesQuery;
  PFN_WDF_DEVICE_RESOURCE_REQUIREMENTS_QUERY EvtDeviceResourceRequirementsQuery;
  PFN_WDF_DEVICE_EJECT                       EvtDeviceEject;
  PFN_WDF_DEVICE_SET_LOCK                    EvtDeviceSetLock;
  PFN_WDF_DEVICE_ENABLE_WAKE_AT_BUS          EvtDeviceEnableWakeAtBus;
  PFN_WDF_DEVICE_DISABLE_WAKE_AT_BUS         EvtDeviceDisableWakeAtBus;
  PFN_WDF_DEVICE_REPORTED_MISSING            EvtDeviceReportedMissing;
} WDF_PDO_EVENT_CALLBACKS, *PWDF_PDO_EVENT_CALLBACKS;
````

## Members

        
            `EvtDeviceDisableWakeAtBus`

            A pointer to the driver's <a href="..\wdfpdo\nc-wdfpdo-evt_wdf_device_disable_wake_at_bus.md">EvtDeviceDisableWakeAtBus</a> event callback function, or <b>NULL</b>.
        
            `EvtDeviceEject`

            A pointer to the driver's <a href="..\wdfpdo\nc-wdfpdo-evt_wdf_device_eject.md">EvtDeviceEject</a> event callback function, or <b>NULL</b>.
        
            `EvtDeviceEnableWakeAtBus`

            A pointer to the driver's <a href="..\wdfpdo\nc-wdfpdo-evt_wdf_device_enable_wake_at_bus.md">EvtDeviceEnableWakeAtBus</a> event callback function, or <b>NULL</b>.
        
            `EvtDeviceReportedMissing`

            A pointer to the driver's <a href="..\wdfpdo\nc-wdfpdo-evt_wdf_device_reported_missing.md">EvtDeviceReportedMissing</a> event callback function, or <b>NULL</b>. The <b>EvtDeviceReportedMissing</b> member is available in version 1.11 and later versions of KMDF.
        
            `EvtDeviceResourceRequirementsQuery`

            A pointer to the driver's <a href="..\wdfpdo\nc-wdfpdo-evt_wdf_device_resource_requirements_query.md">EvtDeviceResourceRequirementsQuery</a> event callback function, or <b>NULL</b>.
        
            `EvtDeviceResourcesQuery`

            A pointer to the driver's <a href="https://msdn.microsoft.com/3210b28b-cbaa-4ad9-9ca8-3b5f03aee41e">EvtDeviceResourcesQuery</a> event callback function, or <b>NULL</b>.
        
            `EvtDeviceSetLock`

            A pointer to the driver's <a href="..\wdfpdo\nc-wdfpdo-evt_wdf_device_set_lock.md">EvtDeviceSetLock</a> event callback function, or <b>NULL</b>.
        
            `Size`

            The size, in bytes, of this structure.

    ## Remarks
        The <b>WDF_PDO_EVENT_CALLBACKS</b> structure is used as input to <a href="..\wdfpdo\nf-wdfpdo-wdfpdoinitseteventcallbacks.md">WdfPdoInitSetEventCallbacks</a>.

Drivers must call <a href="..\wdfpdo\nf-wdfpdo-wdf_pdo_event_callbacks_init.md">WDF_PDO_EVENT_CALLBACKS_INIT</a> to initialize this structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** |  |
| **Header** | wdfpdo.h (include Wdf.h) |

    ## See Also

        <dl>
<dt>
<a href="..\wdffdo\ns-wdffdo-_wdf_fdo_event_callbacks.md">WDF_FDO_EVENT_CALLBACKS</a>
</dt>
<dt>
<a href="..\wdffdo\nf-wdffdo-wdffdoinitseteventcallbacks.md">WdfFdoInitSetEventCallbacks</a>
</dt>
<dt>
<a href="..\wdfpdo\nf-wdfpdo-wdf_pdo_event_callbacks_init.md">WDF_PDO_EVENT_CALLBACKS_INIT</a>
</dt>
<dt>
<a href="..\wdfpdo\nf-wdfpdo-wdfpdoinitseteventcallbacks.md">WdfPdoInitSetEventCallbacks</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_PDO_EVENT_CALLBACKS structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>