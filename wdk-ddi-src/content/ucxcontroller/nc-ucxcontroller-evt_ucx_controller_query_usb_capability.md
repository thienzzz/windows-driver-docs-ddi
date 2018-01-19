---
UID : NC:ucxcontroller.EVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY
title : EVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY
author : windows-driver-content
description : The client driver's implementation to determine if the controller supports a specific capability.
old-location : buses\evt_ucx_controller_query_usb_capability.htm
old-project : usbref
ms.assetid : c01150b6-e6cf-484c-be3e-c63984e97bb3
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : UcxInitializeDeviceInit
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : ucxcontroller.h
req.include-header : Ucxclass.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 2.0
req.alt-api : PEVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY
req.alt-loc : Ucxcontroller.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : UCM_PD_REQUEST_DATA_OBJECT, *PUCM_PD_REQUEST_DATA_OBJECT
req.product : Windows 10 or later.
---


# EVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY function
The client driver's implementation to determine if the controller supports a specific capability.

## Syntax

```
EVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY EvtUcxControllerQueryUsbCapability;

_IRQL_requires_same_ NTSTATUS EvtUcxControllerQueryUsbCapability(
  UCXCONTROLLER UcxController,
  PGUID CapabilityType,
  ULONG OutputBufferLength,
  PVOID OutputBuffer,
  PULONG ResultLength
)
{...}
```

## Parameters

`UcxController`

A handle to the UCX controller that the client driver received in a previous call to  the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188033">UcxControllerCreate</a> method.

`CapabilityType`

Pointer to a GUID specifying the requested capability. The possible  <i>PGUID</i>  values are  as follows:

<ul>
<li>GUID_USB_CAPABILITY_CHAINED_MDLS</li>
<li>GUID_USB_CAPABILITY_STATIC_STREAMS</li>
<li>GUID_USB_CAPABILITY_SELECTIVE_SUSPEND</li>
<li>GUID_USB_CAPABILITY_FUNCTION_SUSPEND

</li>
<li>GUID_USB_CAPABILITY_DEVICE_CONNECTION_HIGH_SPEED_COMPATIBLE</li>
<li>GUID_USB_CAPABILITY_DEVICE_CONNECTION_SUPER_SPEED_COMPATIBLE</li>
<li>GUID_USB_CAPABILITY_CLEAR_TT_BUFFER_ON_ASYNC_TRANSFER_CANCEL<ul>
<li>For typical host controllers, the query must fail (STATUS_NOT_SUPPORTED). If the controller succeeds this capability, it is requesting a Clear TT Buffer when canceling Low Speed/Full Speed asynchronous (Bulk or Control) transfers that have been sent to a TT hub.</li>
</ul>
</li>
</ul>
   See the Remarks section of <a href="https://msdn.microsoft.com/library/windows/hardware/hh406230">USBD_QueryUsbCapability</a> for more information.

`OutputBufferLength`

The length, in bytes, of the request's output buffer, if an output buffer is available.

`OutputBuffer`

A pointer to a location that receives the buffer's address. Certain capabilities may need to provide additional information
        to UCX in this buffer.

`ResultLength`

A location that, on return, contains the size, in bytes, of the information that the callback function stored in <i>OutputBuffer.</i>


## Return Value

If the operation is successful, the callback function must return STATUS_SUCCESS, or another status value for which NT_SUCCESS(status) equals TRUE. Otherwise it must return a status value for which NT_SUCCESS(status) equals FALSE.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The requested USB capability is supported.
<dl>
<dt><b>STATUS_NOT_IMPLEMENTED</b></dt>
</dl>The requested USB capability is unknown and not supported.
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>Controller does not support the requested USB capability.

For GUID_USB_CAPABILITY_CLEAR_TT_BUFFER_ON_ASYNC_TRANSFER_CANCEL, the controller did not request a Clear TT Buffer when canceling Low Speed/Full Speed
        asynchronous (Bulk or Control) transfers that were sent to a TT hub.

## Remarks

The UCX client driver registers its <i>EVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY</i> implementation with the USB host controller extension (UCX) by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188033">UcxControllerCreate</a> method.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** | 2.0 |
| **Header** | ucxcontroller.h (include Ucxclass.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt188033">UcxControllerCreate</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20EVT_UCX_CONTROLLER_QUERY_USB_CAPABILITY callback function%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>