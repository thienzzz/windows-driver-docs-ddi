---
UID : NC:wsk.PFN_WSK_CONTROL_CLIENT
title : PFN_WSK_CONTROL_CLIENT
author : windows-driver-content
description : The WskControlClient function performs control operations on a WSK client object.
old-location : netvista\wskcontrolclient.htm
old-project : netvista
ms.assetid : dad13c60-3511-4641-9182-71a1ce032a69
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WPP_TRIAGE_INFO, *PWPP_TRIAGE_INFO, WPP_TRIAGE_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : wsk.h
req.include-header : Wsk.h
req.target-type : Universal
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WskControlClient
req.alt-loc : wsk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : "*PWPP_TRIAGE_INFO, WPP_TRIAGE_INFO"
req.product : Windows 10 or later.
---


# PFN_WSK_CONTROL_CLIENT callback function
The 
  <b>WskControlClient</b> function performs control operations on a WSK client object.

## Syntax

```
PFN_WSK_CONTROL_CLIENT PfnWskControlClient;

NTSTATUS PfnWskControlClient(
  PWSK_CLIENT Client,
  ULONG ControlCode,
  SIZE_T InputSize,
  PVOID InputBuffer,
  SIZE_T OutputSize,
  PVOID OutputBuffer,
  SIZE_T *OutputSizeReturned,
  PIRP Irp
)
{...}
```

## Parameters

`Client`

A pointer to a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff571155">WSK_CLIENT</a> structure that was returned through
     the 
     <i>WskProviderNpi</i> parameter of the 
     <a href="..\wsk\nf-wsk-wskcaptureprovidernpi.md">
     WskCaptureProviderNPI function.

`ControlCode`

The control operation that is being performed. A WSK application can specify one of the following
     control codes:

`InputSize`

The number of bytes of data in the buffer that is pointed to by the 
     <i>InputBuffer</i> parameter.

`InputBuffer`

A caller-allocated buffer that supplies any input data that is required to perform the specified
     control operation. If no input data is required for the specified control operation, the WSK application
     should set this parameter to <b>NULL</b> and set the 
     <i>InputSize</i> parameter to zero.

`OutputSize`

The size, in bytes, of the buffer that is pointed to by the 
     <i>OutputBuffer</i> parameter.

`OutputBuffer`

A caller-allocated buffer that receives any output data that is returned by the specified control
     operation. If no output data is returned by the specified control operation, the WSK application should
     set this parameter to <b>NULL</b> and set the 
     <i>OutputSize</i> parameter to zero.

`*OutputSizeReturned`



`Irp`

A pointer to a caller-allocated IRP that the WSK subsystem uses to complete the control operation
     asynchronously. For more information about using IRPs with WSK functions, see 
     <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/using-irps-with-winsock-kernel-functions">Using IRPs with Winsock
     Kernel Functions</a>.
     

This parameter is required, is optional, or must be <b>NULL</b>, depending on the particular client control
     operation that is being performed. For more information about the requirements for this parameter for
     each of the supported client control operations, see 
     <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff571157">WSK Client Control
     Operations</a>.


## Return Value

<b>WskControlClient</b> returns one of the following NTSTATUS codes:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The control operation completed successfully. If the WSK application specified a pointer to an
       IRP in the 
       <i>Irp</i> parameter, the IRP will be completed with success status.
<dl>
<dt><b>STATUS_PENDING</b></dt>
</dl>The WSK subsystem could not complete the control operation immediately. The WSK subsystem will
       complete the IRP after it has completed the control operation. The status of the control operation
       will be returned in the 
       <b>IoStatus.Status</b> field of the IRP.
<dl>
<dt><b>STATUS_BUFFER_OVERFLOW</b></dt>
</dl>The output buffer is not large enough to contain the returned data. The variable that is pointed
       to by the 
       <i>OutputSizeReturned</i> parameter contains the required buffer size.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred. The IRP will be completed with failure status.

## Remarks

For more information about how the input and output buffers are used for each client control
    operation, see 
    <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff571157">WSK Client Control
    Operations</a>.

If the 
    <b>WskControlClient</b> function returns STATUS_PENDING, any buffers that are pointed to by the 
    <i>InputBuffer</i> parameter or the 
    <i>OutputBuffer</i> parameter must remain valid until the IRP is completed. If the WSK application
    allocated the buffers with one of the 
    <b>ExAllocate<i>Xxx</i></b> functions, it cannot free the memory with the corresponding 
    <b>ExFree<i>Xxx</i></b> function until after the IRP is completed. If the WSK application allocated the buffers on the
    stack, it cannot return from the function that calls the 
    <b>WskControlClient</b> function until after the IRP is completed.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wsk.h (include Wsk.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wsk\nf-wsk-wskcaptureprovidernpi.md">WskCaptureProviderNPI</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff571155">WSK_CLIENT</a>
</dt>
<dt>
<a href="..\wsk\ns-wsk-_wsk_provider_dispatch.md">WSK_PROVIDER_DISPATCH</a>
</dt>
<dt>
<a href="..\wsk\ns-wsk-_wsk_provider_npi.md">WSK_PROVIDER_NPI</a>
</dt>
<dt>
<a href="..\wsk\ns-wsk-_wsk_transport.md">WSK_TRANSPORT</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff571157">WSK Client Control Operations</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20PFN_WSK_CONTROL_CLIENT callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>