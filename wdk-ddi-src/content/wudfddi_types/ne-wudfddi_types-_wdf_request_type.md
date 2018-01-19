---
UID : NE:wudfddi_types._WDF_REQUEST_TYPE
title : _WDF_REQUEST_TYPE
author : windows-driver-content
description : The WDF_REQUEST_TYPE enumeration identifies the types of I/O requests that a UMDF request object can represent.
old-location : wdf\wdf_request_type__umdf_.htm
old-project : wdf
ms.assetid : a883f22e-0d6f-4755-882b-ad5a60a09271
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDF_REQUEST_TYPE, WDF_REQUEST_TYPE, *PWDF_REQUEST_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wudfddi_types.h
req.include-header : Wudfddi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WDF_REQUEST_TYPE
req.alt-loc : Wudfddi_types.h
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
req.typenames : WDF_REQUEST_TYPE, *PWDF_REQUEST_TYPE
req.product : Windows 10 or later.
---

# _WDF_REQUEST_TYPE Enumeration
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]


      The <b>WDF_REQUEST_TYPE</b> enumeration identifies the types of I/O requests that a UMDF request object can represent.

## Syntax
````
typedef enum _WDF_REQUEST_TYPE { 
  WdfRequestUndefined          = 0,
  WdfRequestCreate             = 1,
  WdfRequestCleanup            = 2,
  WdfRequestRead               = 3,
  WdfRequestWrite              = 4,
  WdfRequestDeviceIoControl    = 5,
  WdfRequestClose              = 6,
  WdfRequestUsb                = 7,
  WdfRequestOther              = 8,
  WdfRequestInternalIoctl      = 9,
  WdfRequestTypeNoFormat       = 10,
  WdfRequestFlushBuffers       = 11,
  WdfRequestQueryInformation   = 12,
  WdfRequestSetInformation     = 13,
  WdfRequestMaximum
} WDF_REQUEST_TYPE;
````

## Constants

<table>

<tr>
<td>WdfRequestCleanup</td>
<td>The request object represents a file cleanup request. The driver receives this type of request object after an application's call to the Win32 <b>CloseHandle</b> function closes the last handle to a file object, but possibly before all of the file's outstanding I/O requests have been completed or canceled. The framework delivers this type of request to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff554905">IFileCallbackCleanup::OnCleanupFile</a> callback function. (Also see <b>WdfRequestClose</b>.)</td>
</tr>

<tr>
<td>WdfRequestClose</td>
<td>The request object represents a file close request.  The driver receives this type of request object after an application's call to the Win32 <b>CloseHandle</b> function closes the last handle to a file object, and after all of the file's outstanding I/O requests have been completed or canceled.  The framework delivers this type of request to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff554910">IFileCallbackClose::OnCloseFile</a> callback function. (Also see <b>WdfRequestCleanup</b>.)</td>
</tr>

<tr>
<td>WdfRequestCreate</td>
<td>The request object represents a file creation request. The driver receives this type of request object when an application opens a device by calling the Microsoft Win32 <b>CreateFile</b> function. The framework delivers this type of request, along with a newly created file object (<a href="..\wudfddi\nn-wudfddi-iwdffile.md">IWDFFile</a>), to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556841">IQueueCallbackCreate::OnCreateFile</a> callback function. The new file object represents the HANDLE-typed file handle that the Win32 <b>CreateFile</b> returns.</td>
</tr>

<tr>
<td>WdfRequestDeviceIoControl</td>
<td>The request object represents a device I/O control request. This driver receives this type of I/O request when an application calls the Win32 <b>DeviceIoControl</b> function. The framework delivers this type of request to  the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556854">IQueueCallbackDeviceIoControl::OnDeviceIoControl</a> callback function.</td>
</tr>

<tr>
<td>WdfRequestFlushBuffers</td>
<td>The request object represents a request to flush cached buffers. The framework delivers this type of request to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556847">IQueueCallbackDefaultIoHandler::OnDefaultIoHandler</a> callback function.</td>
</tr>

<tr>
<td>WdfRequestInternalIoctl</td>
<td>This value is reserved for internal use only.</td>
</tr>

<tr>
<td>WdfRequestMaximum</td>
<td>The maximum value for the enumeration is exceeded.</td>
</tr>

<tr>
<td>WdfRequestOther</td>
<td>This value is reserved for internal use only.</td>
</tr>

<tr>
<td>WdfRequestQueryInformation</td>
<td>The request object represents a request to obtain information about a file. The framework delivers this type of request to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556847">IQueueCallbackDefaultIoHandler::OnDefaultIoHandler</a> callback function.</td>
</tr>

<tr>
<td>WdfRequestRead</td>
<td>The request object represents a read request. This driver receives this type of I/O request when an application calls the Win32 <b>ReadFile</b> or <b>ReadFileEx</b> function. The framework delivers this type of request to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556875">IQueueCallbackRead::OnRead</a> callback function.</td>
</tr>

<tr>
<td>WdfRequestSetInformation</td>
<td>The request object represents a request to set information about a file. The framework delivers this type of request to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556847">IQueueCallbackDefaultIoHandler::OnDefaultIoHandler</a> callback function.</td>
</tr>

<tr>
<td>WdfRequestTypeNoFormat</td>
<td>The request object's type has not been specified.</td>
</tr>

<tr>
<td>WdfRequestUndefined</td>
<td>The type of the request object is undefined.</td>
</tr>

<tr>
<td>WdfRequestUsb</td>
<td>The request object was sent to a USB port. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560296">IWDFRequestCompletionParams::GetCompletedRequestType</a> method can return this value.</td>
</tr>

<tr>
<td>WdfRequestWrite</td>
<td>The request object represents a write request. This driver receives this type of I/O request when an application calls the Win32 <b>WriteFile</b> or <b>WriteFileEx</b> function. The framework delivers this type of request to  the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556885">IQueueCallbackWrite::OnWrite</a> callback function.</td>
</tr>
</table>

## Remarks

The <b>WDF_REQUEST_TYPE</b> enumeration is used as an input parameter of <a href="https://msdn.microsoft.com/library/windows/hardware/ff557014">IWDFDevice::ConfigureRequestDispatching</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff558946">IWDFIoQueue::ConfigureRequestDispatching</a>. It is also used for the return value of <a href="https://msdn.microsoft.com/library/windows/hardware/ff559124">IWDFIoRequest::GetType</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff560296">IWDFRequestCompletionParams::GetCompletedRequestType</a>.

For the KMDF version of this enumeration, see <a href="..\wudfddi_types\ne-wudfddi_types-_wdf_request_type.md">WDF_REQUEST_TYPE</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wudfddi_types.h (include Wudfddi.h) |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554905">IFileCallbackCleanup::OnCleanupFile</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554910">IFileCallbackClose::OnCloseFile</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556841">IQueueCallbackCreate::OnCreateFile</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556854">IQueueCallbackDeviceIoControl::OnDeviceIoControl</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556875">IQueueCallbackRead::OnRead</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556885">IQueueCallbackWrite::OnWrite</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdffile.md">IWDFFile</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_REQUEST_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>