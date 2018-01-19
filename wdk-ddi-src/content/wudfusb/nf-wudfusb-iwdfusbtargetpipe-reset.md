---
UID : NF:wudfusb.IWDFUsbTargetPipe.Reset
title : IWDFUsbTargetPipe::Reset method
author : windows-driver-content
description : The Reset method resets the data toggle and clears the stall condition on a USB pipe.
old-location : wdf\iwdfusbtargetpipe_reset.htm
old-project : wdf
ms.assetid : 8d42dd60-a032-4486-87e0-2204e833035b
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : IWDFUsbTargetPipe, IWDFUsbTargetPipe::Reset, Reset
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : wudfusb.h
req.include-header : Wudfusb.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 1.5
req.alt-api : IWDFUsbTargetPipe.Reset
req.alt-loc : WUDFx.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : Unavailable in UMDF 2.0 and later.
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : WUDFx.dll
req.irql : 
req.typenames : "*PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE"
req.product : Windows 10 or later.
---


# Reset method
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>Reset</b> method resets the data toggle and clears the stall condition on a USB pipe.

## Syntax

````
HRESULT  Reset();
````

## Parameters

This function has no parameters.

## Return Value

<b>Reset</b> returns one of the following values:
<dl>
<dt><b>S_OK </b></dt>
</dl>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> successfully reset the data toggle and cleared the stall condition. 
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> encountered an allocation failure.
<dl>
<dt><b>An error code that is defined in Winerror.h</b></dt>
</dl>This value corresponds to the error code that the WinUsb API returned.

 

<b>Reset</b> returns one of the following values:
<dl>
<dt><b>S_OK </b></dt>
</dl>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> successfully reset the data toggle and cleared the stall condition. 
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> encountered an allocation failure.
<dl>
<dt><b>An error code that is defined in Winerror.h</b></dt>
</dl>This value corresponds to the error code that the WinUsb API returned.

 

<b>Reset</b> returns one of the following values:
<dl>
<dt><b>S_OK </b></dt>
</dl>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> successfully reset the data toggle and cleared the stall condition. 
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> encountered an allocation failure.
<dl>
<dt><b>An error code that is defined in Winerror.h</b></dt>
</dl>This value corresponds to the error code that the WinUsb API returned.

## Remarks

The <b>Reset</b> method generates a UMDF request and synchronously sends the request to the I/O target.

For more information about how <b>Reset</b> works, see the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540300">WinUsb_ResetPipe</a> function.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** | 1.5 |
| **Header** | wudfusb.h (include Wudfusb.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wudfusb\nn-wudfusb-iwdfusbtargetpipe.md">IWDFUsbTargetPipe</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540300">WinUsb_ResetPipe</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFUsbTargetPipe::Reset method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>