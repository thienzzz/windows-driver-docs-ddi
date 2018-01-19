---
UID : NF:wdfusb.WdfUsbTargetPipeSetNoMaximumPacketSizeCheck
title : WdfUsbTargetPipeSetNoMaximumPacketSizeCheck function
author : windows-driver-content
description : The WdfUsbTargetPipeSetNoMaximumPacketSizeCheck method disables the framework's test of whether the size of a driver's read buffer is a multiple of a USB pipe's maximum packet size.
old-location : wdf\wdfusbtargetpipesetnomaximumpacketsizecheck.htm
old-project : wdf
ms.assetid : 552eaf46-1710-4df5-bdc3-0fa7ce3adf54
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WdfUsbTargetPipeSetNoMaximumPacketSizeCheck
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfusb.h
req.include-header : Wdfusb.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 2.0
req.alt-api : WdfUsbTargetPipeSetNoMaximumPacketSizeCheck
req.alt-loc : Wdf01000.sys,Wdf01000.sys.dll,WUDFx02000.dll,WUDFx02000.dll.dll
req.ddi-compliance : DriverCreate, KmdfIrql, KmdfIrql2, UsbKmdfIrql, UsbKmdfIrql2
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Wdf01000.sys (KMDF); WUDFx02000.dll (UMDF)
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : "*PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE"
req.product : Windows 10 or later.
---


# WdfUsbTargetPipeSetNoMaximumPacketSizeCheck function
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WdfUsbTargetPipeSetNoMaximumPacketSizeCheck</b> method disables the framework's test of whether the size of a driver's read buffer is a multiple of a USB pipe's maximum packet size.

## Syntax

````
VOID WdfUsbTargetPipeSetNoMaximumPacketSizeCheck(
  _In_ WDFUSBPIPE Pipe
);
````

## Parameters

`Pipe`

A handle to a framework pipe object that was obtained by calling <a href="..\wdfusb\nf-wdfusb-wdfusbinterfacegetconfiguredpipe.md">WdfUsbInterfaceGetConfiguredPipe</a>.


## Return Value

None.

A bug check occurs if the driver supplies an invalid object handle.

## Remarks

To avoid receiving extra data from unexpected bus activity, which is sometimes called <i>babble</i>, drivers usually specify read buffers that are a multiple of the pipe's maximum packet size. (Drivers receive a USB pipe's maximum packet size in a <a href="..\wdfusb\ns-wdfusb-_wdf_usb_pipe_information.md">WDF_USB_PIPE_INFORMATION</a> structure.) By default, the framework reports an error if a driver specifies a read buffer that is not a multiple of the pipe's maximum packet size. If the driver calls <b>WdfUsbTargetPipeSetNoMaximumPacketSizeCheck</b>, the framework does not report an error if a read buffer is not a multiple of the maximum packet size.

For more information about the <b>WdfUsbTargetPipeSetNoMaximumPacketSizeCheck</b> method and USB I/O targets, see <a href="https://msdn.microsoft.com/195c0f4b-7f33-428a-8de7-32643ad854c6">USB I/O Targets</a>.

The following code example disables the framework's test of whether the size of a buffer is a multiple of a USB pipe's maximum packet size.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfusb.h (include Wdfusb.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** | DriverCreate, KmdfIrql, KmdfIrql2, UsbKmdfIrql, UsbKmdfIrql2 |

## See Also

<dl>
<dt>
<a href="..\wdfusb\ns-wdfusb-_wdf_usb_pipe_information.md">WDF_USB_PIPE_INFORMATION</a>
</dt>
<dt>
<a href="..\wdfusb\nf-wdfusb-wdfusbinterfacegetconfiguredpipe.md">WdfUsbInterfaceGetConfiguredPipe</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfUsbTargetPipeSetNoMaximumPacketSizeCheck method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>