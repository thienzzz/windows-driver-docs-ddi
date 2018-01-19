---
UID : NF:wdfresource.WdfCmResourceListRemove
title : WdfCmResourceListRemove function
author : windows-driver-content
description : The WdfCmResourceListRemove method removes a resource descriptor from a specified resource list.
old-location : wdf\wdfcmresourcelistremove.htm
old-project : wdf
ms.assetid : f636d85d-f7bb-4ebe-b03f-3b9c3c17bacd
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WdfCmResourceListRemove
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfresource.h
req.include-header : Wdf.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 
req.alt-api : WdfCmResourceListRemove
req.alt-loc : Wdf01000.sys,Wdf01000.sys.dll
req.ddi-compliance : DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Wdf01000.sys (see Framework Library Versioning.)
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : "*PWDF_REQUEST_SEND_OPTIONS, WDF_REQUEST_SEND_OPTIONS"
req.product : Windows 10 or later.
---


# WdfCmResourceListRemove function
<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfCmResourceListRemove</b> method removes a resource descriptor from a specified resource list.

## Syntax

````
VOID WdfCmResourceListRemove(
  _In_ WDFCMRESLIST List,
  _In_ ULONG        Index
);
````

## Parameters

`List`

A handle to a framework resource-list object that represents a list of hardware resources for a device.

`Index`

A zero-based value that is used as an index into the resource list that <i>List</i> specifies.


## Return Value

None.

A system bug check occurs if the driver supplies an invalid object handle.

## Remarks

The <b>WdfCmResourceListRemove</b> method removes the resource descriptor that is associated with the index value that the <i>Index</i> parameter specifies.

When <b>WdfCmResourceListRemove</b> removes the resource descriptor that has the index value <i>n</i>, the index value of the next resource descriptor changes from <i>n</i>+1 to <i>n</i>.

For more information about resource lists, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/hardware-resources-for-kmdf-drivers">Hardware Resources for Framework-Based Drivers</a>.

The following code example removes the third resource descriptor from the raw and translated lists of hardware resources that an <a href="..\wdffdo\nc-wdffdo-evt_wdf_device_remove_added_resources.md">EvtDeviceRemoveAddedResources</a> callback function receives.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** |  |
| **Header** | wdfresource.h (include Wdf.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** | DriverCreate, KmdfIrql, KmdfIrql2 |

## See Also

<dl>
<dt>
<a href="..\wdfresource\nf-wdfresource-wdfcmresourcelistremovebydescriptor.md">WdfCmResourceListRemoveByDescriptor</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfCmResourceListRemove method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>