---
UID : NF:portcls.IUnregisterPhysicalConnection.UnregisterPhysicalConnectionToExternal
title : IUnregisterPhysicalConnection::UnregisterPhysicalConnectionToExternal method
author : windows-driver-content
description : The UnregisterPhysicalConnectionToExternal method deletes the registration of a physical connection that was registered by a previous call to PcRegisterPhysicalConnectionToExternal.
old-location : audio\iunregisterphysicalconnection_unregisterphysicalconnectiontoexternal.htm
old-project : audio
ms.assetid : 250bf99c-d5fa-459b-bd94-d438368379f1
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : IUnregisterPhysicalConnection, IUnregisterPhysicalConnection::UnregisterPhysicalConnectionToExternal, UnregisterPhysicalConnectionToExternal
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : portcls.h
req.include-header : Portcls.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IUnregisterPhysicalConnection.UnregisterPhysicalConnectionToExternal
req.alt-loc : portcls.h
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
req.typenames : PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---


# UnregisterPhysicalConnectionToExternal method
The <code>UnregisterPhysicalConnectionToExternal</code> method deletes the registration of a physical connection that was registered by a previous call to <a href="..\portcls\nf-portcls-pcregisterphysicalconnectiontoexternal.md">PcRegisterPhysicalConnectionToExternal</a>.

## Syntax

````
NTSTATUS UnregisterPhysicalConnectionToExternal(
  [in] PDEVICE_OBJECT  DeviceObject,
  [in] PUNKNOWN        FromUnknown,
  [in] ULONG           FromPin,
  [in] PUNICODE_STRING ToString,
  [in] ULONG           ToPin
);
````

## Parameters

`DeviceObject`

Pointer to the device object for the adapter device. This parameter must point to a system structure of type <a href="..\wdm\ns-wdm-_device_object.md">DEVICE_OBJECT</a>.

`FromUnknown`

Pointer to the <a href="..\portcls\nn-portcls-iport.md">IPort</a> interface of a port driver object. The port driver object that is associated with <i>FromUnknown</i> is bound to the subdevice that supplies the connection's data source pin.

`FromPin`

Specifies a pin ID. This parameter identifies the data source (output) pin on the filter that is associated with the <i>FromUnknown</i> interface.

`ToString`

Pointer to a null-terminated Unicode string that contains the name of the external filter that supplies the connection's data sink pin.

`ToPin`

Specifies a pin ID. This parameter identifies the data sink (input) pin on the external filter that is named by the <i>ToString</i> parameter.


## Return Value

<b>UnregisterPhysicalConnectionToExternal</b> returns STATUS_SUCCESS if the call was successful. Otherwise, it returns an appropriate error code.

## Remarks

For more information, see <a href="https://msdn.microsoft.com/d8ebd6d9-37ed-4890-aae1-5ecf58f2e22a">Dynamic Audio Subdevices</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | portcls.h (include Portcls.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\portcls\nn-portcls-iunregisterphysicalconnection.md">IUnregisterPhysicalConnection</a>
</dt>
<dt>
<a href="..\portcls\nf-portcls-pcregisterphysicalconnectiontoexternal.md">PcRegisterPhysicalConnectionToExternal</a>
</dt>
<dt>
<a href="..\wdm\ns-wdm-_device_object.md">DEVICE_OBJECT</a>
</dt>
<dt>
<a href="..\portcls\nn-portcls-iport.md">IPort</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IUnregisterPhysicalConnection::UnregisterPhysicalConnectionToExternal method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>