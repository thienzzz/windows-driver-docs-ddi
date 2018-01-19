---
UID : NF:ntddk.IoFreeController
title : IoFreeController function
author : windows-driver-content
description : The IoFreeController routine releases a previously allocated controller object when the driver has completed an I/O request.
old-location : kernel\iofreecontroller.htm
old-project : kernel
ms.assetid : a9b0ca27-dc46-4f9b-a3f9-51bbd759afc1
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : IoFreeController
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoFreeController
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : IrqlDispatch, HwStorPortProhibitedDDIs, IrqlDispatch(storport)
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : DISPATCH_LEVEL
req.typenames : WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---


# IoFreeController function
The <b>IoFreeController</b> routine releases a previously allocated controller object when the driver has completed an I/O request.

## Syntax

````
VOID IoFreeController(
  _In_ PCONTROLLER_OBJECT ControllerObject
);
````

## Parameters

`ControllerObject`

Pointer to the driver's controller object, which was allocated for the current I/O operation on a particular device by calling <b>IoAllocateController</b>.


## Return Value

None

## Remarks

The connection between the current target device object and the controller object is released only if no requests are currently queued to the same device. Otherwise, the driver's ControllerControl routine is called with the next IRP bound through the device controller to the target device.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h) |
| **Library** |  |
| **IRQL** | DISPATCH_LEVEL |
| **DDI compliance rules** | IrqlDispatch, HwStorPortProhibitedDDIs, IrqlDispatch(storport) |

## See Also

<dl>
<dt>
<a href="..\ntddk\nf-ntddk-ioallocatecontroller.md">IoAllocateController</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-iocreatecontroller.md">IoCreateController</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-iodeletecontroller.md">IoDeleteController</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IoFreeController routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>