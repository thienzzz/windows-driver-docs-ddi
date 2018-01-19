---
UID : NF:ucmtcpciportcontroller.UcmTcpciPortControllerStart
title : UcmTcpciPortControllerStart function
author : windows-driver-content
description : Indicates to the UcmTcpciCx class extension that the client driver is now ready to service hardware requests for the port controller.
old-location : buses\ucmtcpciportcontrollerstart.htm
old-project : usbref
ms.assetid : 94e7c36a-e45c-4d98-aeb7-f23769347ca5
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : UcmTcpciPortControllerStart
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ucmtcpciportcontroller.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : UcmTcpciPortControllerStart
req.alt-loc : ucmtcpcicxstub.lib,ucmtcpcicxstub.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ucmtcpcicxstub.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : UCMTCPCI_PORT_CONTROLLER_ALERT_TYPE
req.product : Windows 10 or later.
---


# UcmTcpciPortControllerStart function
Indicates to the UcmTcpciCx class extension that the client driver  is now ready to service hardware requests for the port controller.

## Syntax

````
NTSTATUS UcmTcpciPortControllerStart(
   UCMTCPCIPORTCONTROLLER PortControllerObject
);
````

## Parameters

`PortControllerObject`

Handle to the port controller  object that the client driver received in the previous call to <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollercreate.md">UcmTcpciPortControllerCreate</a>.


## Return Value

(NTSTATUS) The method returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method may return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.
                    
<dl>
<dt><b>STATUS_INVALID_DEVICE_REQUEST</b></dt>
</dl>The port controller is already in Start state.
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>Hardware request queue has not been set by calling <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollersethardwarerequestqueue.md">UcmTcpciPortControllerSetHardwareRequestQueue</a>.

## Remarks

After the client driver has received the UCMPORTCONTROLLER handle for the port controller object, the driver calls this method to notify the class extension that the driver can start receiving hardware requests. This method call allows the client driver to perform initialization of its framework context space on the port controller object, before the class extension can invoke the driver's callback functions or requests for the port controller object. The driver cannot call <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrolleralert.md">UcmTcpciPortControllerAlert</a> or  <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollerstop.md">UcmTcpciPortControllerStop</a> until the port controller has been started.

The client driver calls this method right after calling <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollercreate.md">UcmTcpciPortControllerCreate</a> and initializing its context structure, if it was specified in the <a href="..\wdfobject\ns-wdfobject-_wdf_object_attributes.md">WDF_OBJECT_ATTRIBUTES</a> structure as the <i>Attributes</i> parameter value.
The driver must assume that the class extension may submit requests even before <b>UcmTcpciPortControllerStart</b> returns, i.e., from within this DDI call. If the driver is holding a lock while calling <b>UcmTcpciPortControllerStart</b> and also attempts to acquire a lock while handling a hardware request (in its hardware request queue callback), it might result in a deadlock.


A call to <b>UcmTcpciPortControllerStart</b> to start a port controller object already in Start state, results in an error. 


On boot, if the BIOS had already negotiated a PD contract, UcmTcpciCx starts from an unattached state.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ucmtcpciportcontroller.h |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollerstop.md">UcmTcpciPortControllerStop</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UcmTcpciPortControllerStart method%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>