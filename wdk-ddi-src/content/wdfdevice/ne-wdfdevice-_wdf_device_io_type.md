---
UID : NE:wdfdevice._WDF_DEVICE_IO_TYPE
title : _WDF_DEVICE_IO_TYPE
author : windows-driver-content
description : The WDF_DEVICE_IO_TYPE enumeration is used to specify a method for accessing data buffers.
old-location : wdf\wdf_device_io_type.htm
old-project : wdf
ms.assetid : 0ad08e4f-7a9b-4052-888e-ae01c9c105c8
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDF_DEVICE_IO_TYPE, *PWDF_DEVICE_IO_TYPE, WDF_DEVICE_IO_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wdfdevice.h
req.include-header : Wdf.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 2.0
req.alt-api : WDF_DEVICE_IO_TYPE
req.alt-loc : wdfdevice.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : See Remarks section.
req.typenames : "*PWDF_DEVICE_IO_TYPE, WDF_DEVICE_IO_TYPE"
req.product : Windows 10 or later.
---

# _WDF_DEVICE_IO_TYPE Enumeration
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_DEVICE_IO_TYPE</b> enumeration is used to specify a <a href="https://msdn.microsoft.com/f95a0aec-65f9-44c9-8ae5-11bb4d832752">method for accessing data buffers</a>.

## Syntax
````
typedef enum _WDF_DEVICE_IO_TYPE { 
  WdfDeviceIoUndefined         = 0,
  WdfDeviceIoNeither           = 1,
  WdfDeviceIoBuffered          = 2,
  WdfDeviceIoDirect            = 3,
  WdfDeviceIoBufferedOrDirect  = 4
} WDF_DEVICE_IO_TYPE, *PWDF_DEVICE_IO_TYPE;
````

## Constants

<table>

<tr>
<td>WdfDeviceIoBuffered</td>
<td>Buffered I/O will be used to access data buffers.</td>
</tr>

<tr>
<td>WdfDeviceIoBufferedOrDirect</td>
<td>This value is not used by KMDF drivers.

<b>UMDF </b>Buffered I/O or direct I/O will be used to access data buffers.</td>
</tr>

<tr>
<td>WdfDeviceIoDirect</td>
<td>Direct I/O will be used to access data buffers.</td>
</tr>

<tr>
<td>WdfDeviceIoNeither</td>
<td><b>UMDF </b>This value is not used by UMDF drivers. A UMDF driver can access device I/O control requests that specify the METHOD_NEITHER buffer access method by setting the <b>UmdfMethodNeitherAction</b> INF directive and using <b>WdfDeviceIoBuffered</b> or <b>WdfDeviceIoDirect</b>. For more information, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/specifying-wdf-directives-in-inf-files">Specifying WDF Directives in INF Files</a>.

<b>KMDF </b>Neither buffered nor direct I/O will be used to access data buffers.</td>
</tr>

<tr>
<td>WdfDeviceIoUndefined</td>
<td>Reserved for system use.</td>
</tr>
</table>

## Remarks

The <b>WDF_DEVICE_IO_TYPE</b> enumeration is used to specify buffer access method types in the <a href="..\wdfdevice\ns-wdfdevice-_wdf_io_type_config.md">WDF_IO_TYPE_CONFIG</a> structure.

The <a href="..\wdfdevice\ns-wdfdevice-_wdf_io_type_config.md">WDF_IO_TYPE_CONFIG</a> structure is used  as input to <a href="..\wdfdevice\nf-wdfdevice-wdfdeviceinitsetiotypeex.md">WdfDeviceInitSetIoTypeEx</a> and <a href="..\wdfdevice\nf-wdfdevice-wdfdeviceinitsetiotype.md">WdfDeviceInitSetIoType</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfdevice.h (include Wdf.h) |

## See Also

<dl>
<dt>
<a href="..\wdfdevice\ns-wdfdevice-_wdf_io_type_config.md">WDF_IO_TYPE_CONFIG</a>
</dt>
<dt>
<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceinitsetiotype.md">WdfDeviceInitSetIoType</a>
</dt>
<dt>
<a href="..\wdfdevice\nf-wdfdevice-wdfdeviceinitsetiotypeex.md">WdfDeviceInitSetIoTypeEx</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_DEVICE_IO_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>