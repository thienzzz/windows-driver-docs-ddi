---
UID : NI:hidport.IOCTL_UMDF_HID_SET_FEATURE
title : IOCTL_UMDF_HID_SET_FEATURE
author : windows-driver-content
description : The IOCTL_UMDF_HID_GET_FEATURE control code sends a feature report to a HIDClass device.
old-location : hid\ioctl_umdf_hid_set_feature.htm
old-project : hid
ms.assetid : 7FFE7301-1C03-4221-9E3B-412FE89919FB
ms.author : windowsdriverdev
ms.date : 12/21/2017
ms.keywords : HidRegisterMinidriver
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : hidport.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 1.11
req.alt-api : IOCTL_UMDF_HID_SET_FEATURE
req.alt-loc : Hidport.h
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
req.typenames : USAGE_AND_PAGE, *PUSAGE_AND_PAGE
---

# IOCTL_UMDF_HID_SET_FEATURE IOCTL
The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439657">IOCTL_UMDF_HID_GET_FEATURE</a> 
   control code sends a <a href="https://msdn.microsoft.com/477FF911-5A17-4EA5-9403-1D7B4E8B3BA5">feature report</a> to a HIDClass device.

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer
A UMDF-based driver calls <a href="https://msdn.microsoft.com/be3f965b-69fe-4d5e-b1b6-3a370603cd7b">IWDFRequest::GetInputMemory</a> to retrieve a  requester-allocated input buffer that contains a feature report.

The driver retrieves the report ID associated with the top-level collection by calling <a href="https://msdn.microsoft.com/96de6f7a-da1d-44a6-b1f7-44859312a662">IWDFRequest::GetDeviceIoControlParameters</a> and providing the  <i>pOutBufferSize</i> parameter, as shown in the following example.<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>UCHAR reportId;
SIZE_T outBufferSize;

FxRequest-&gt;GetDeviceIoControlParameters(NULL, NULL, &amp;outBufferSize);
reportId = (UCHAR)outBufferSize;
</pre>
</td>
</tr>
</table></span></div>

### Input Buffer Length
None.

### Output Buffer
None.

### Output Buffer Length
The size of the buffer that is retrieved by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff559112">IWDFIoRequest::GetOutputMemory</a>.

### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
I/O Status block
HID minidrivers that carry out the I/O to the device must also:


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | hidport.h |
| **IRQL** |  |

    ## See Also

        <dl>
<dt>
<a href="..\hidclass\ni-hidclass-ioctl_hid_set_feature.md">IOCTL_HID_SET_FEATURE</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439657">IOCTL_UMDF_HID_GET_FEATURE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [hid\wdf]:%20IOCTL_UMDF_HID_SET_FEATURE control code%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>