---
UID : NI:acpiioct.IOCTL_ACPI_EVAL_METHOD_EX
title : IOCTL_ACPI_EVAL_METHOD_EX
author : windows-driver-content
description : A driver for a device can use the IOCTL_ACPI_EVAL_METHOD_EX device control request to synchronously evaluate an ACPI control method that is supported by a child device in the namespace of the device.
old-location : acpi\ioctl_acpi_eval_method_ex.htm
old-project : acpi
ms.assetid : 5c8a1038-efc7-424a-8ef9-fd28d0dcb13c
ms.author : windowsdriverdev
ms.date : 12/31/2017
ms.keywords : _UNIT_ISOCH_PARAMS, *PUNIT_ISOCH_PARAMS, UNIT_ISOCH_PARAMS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : acpiioct.h
req.include-header : Acpiioct.h
req.target-type : Windows
req.target-min-winverclnt : Windows Vista and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IOCTL_ACPI_EVAL_METHOD_EX
req.alt-loc : Acpiioct.h
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
req.typenames : "*PUNIT_ISOCH_PARAMS, UNIT_ISOCH_PARAMS"
---

# IOCTL_ACPI_EVAL_METHOD_EX IOCTL
A driver for a device can use the IOCTL_ACPI_EVAL_METHOD_EX device control request to synchronously evaluate an ACPI control method that is supported by a child device in the namespace of the device. The driver should call <a href="..\wdm\nf-wdm-iobuilddeviceiocontrolrequest.md">IoBuildDeviceIoControlRequest</a> and pass the following input and output parameters to build this request.

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer
Set the <b>IoBuildDeviceIoControlRequest</b> input parameters as follows:

<i>IoControlCode</i> is set to IOCTL_ACPI_EVAL_METHOD_EX.

<i>DeviceObject</i> is set to a pointer to the physical device object (PDO) of the device.

<i>InputBuffer</i> is set to a pointer to an input buffer structure that depends on the type of input arguments to be passed to the control method. For more information about the type input arguments that this IOCTL supports, see the Remarks section later in this topic.

<i>InputBufferLength</i> is set to the size, in bytes, of the input buffer that is supplied by <i>InputBuffer</i>.

<i>OutputBufferLength</i> supplies the size, in bytes, of the output buffer that is supplied by <i>OutputBuffer</i>.

<i>InternalDeviceIoControl</i> is set to <b>FALSE</b>.

<i>Event</i> is set to a pointer to a caller-allocated and initialized event object.

### Input Buffer Length
<i>InputBufferLength</i> is set to the size, in bytes, of the input buffer that is supplied by <i>InputBuffer</i>.

### Output Buffer
Set the <i>IoBuildDeviceIoControlRequest</i> output parameters as follows:

<i>OutputBuffer</i> supplies a pointer to an <a href="..\acpiioct\ns-acpiioct-_acpi_eval_output_buffer_v1.md">ACPI_EVAL_OUTPUT_BUFFER</a> structure that contains the output arguments from the control method.

<i>IoStatusBlock</i> is set to a pointer to an <a href="..\wdm\ns-wdm-_io_status_block.md">IO_STATUS_BLOCK</a> structure.

### Output Buffer Length
<i>OutputBufferLength</i> supplies the size, in bytes, of the output buffer that is supplied by <i>OutputBuffer</i>.

### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
I/O Status block
If the request succeeds, <i>IoStatusBlock</i>-&gt;<b>Status</b> is set to STATUS_SUCCESS; otherwise, the <b>Status</b> member is set to an error code. If the output buffer is not large enough to contain the output buffer header, the <b>Status</b> member is set to STATUS_BUFFER_TOO_SMALL. If the output buffer is large enough to contain the output buffer header, but is not large enough to contain all the output arguments from the control method, the <b>Status</b> member is set to STATUS_BUFFER_OVERFLOW, and  <i>OutputBuffer</i>-&gt;<b>Length</b> is set to the required length of the output buffer.

If the request succeeds, the <i>IoStatusBlock</i>-&gt;<b>Information</b> member is set to the number of bytes that is returned in the output buffer; otherwise, the <b>Information</b> member is set to zero.

    ## Remarks
        A driver for a device can use IOCTL_ACPI_EVAL_METHOD_EX to synchronously evaluate a control method that is supported by a child object in the namespace of the device. The path and name of the control method that is supplied by this request must be either the fully qualified path and name of the method in the ACPI namespace or the path and name of the method relative to the device to which the request is sent. For example, assume that a device named 'ABCD' is an immediate child of the root of an ACPI namespace, that the 'ABCD' device supports a child device named 'CHLD,' and that the 'CHLD' device supports a method named '_FOO.' In this case, to evaluate the '_FOO' method, a driver sends an evaluation request to the 'ABCD' device and supplies either the path and name '\ABCD.CHLD._FOO,' which is the fully qualified path and name in the ACPI namespace, or the path and name 'CHLD._FOO,' which is the path and name relative to the 'ABCD' device in the ACPI namespace.

IOCTL_ACPI_EVAL_METHOD_EX supports the following types of input buffer structures:


<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_EX</a>



<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_simple_integer_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_SIMPLE_INTEGER_EX</a>



<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_simple_string_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_SIMPLE_STRING_EX</a>



<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_complex_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_COMPLEX_EX</a>


The output arguments from the control method are returned in the variable-length <a href="..\acpiioct\ns-acpiioct-_acpi_eval_output_buffer_v1.md">ACPI_EVAL_OUTPUT_BUFFER</a> structure that is supplied by the <i>OutBuffer</i> pointer. The ACPI_EVAL_OUTPUT_BUFFER includes an array of variable-length <a href="..\acpiioct\ns-acpiioct-_acpi_method_argument_v1.md">ACPI_METHOD_ARGUMENT</a> structures, each one of which returns an output argument.

For more information about how to synchronously evaluate control methods, see <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/acpi/evaluating-acpi-control-methods-synchronously">Evaluating ACPI Control Methods Synchronously</a>.

A driver can also use an <a href="..\acpiioct\ni-acpiioct-ioctl_acpi_eval_method.md">IOCTL_ACPI_EVAL_METHOD</a> request to synchronously evaluate a control method that is an immediate child object of a device.

For information about how to evaluate an ACPI control method asynchronously starting on Windows Server 2008 and Windows Vista, see <a href="..\acpiioct\ni-acpiioct-ioctl_acpi_async_eval_method.md">IOCTL_ACPI_ASYNC_EVAL_METHOD</a> and <a href="..\acpiioct\ni-acpiioct-ioctl_acpi_async_eval_method_ex.md">IOCTL_ACPI_ASYNC_EVAL_METHOD_EX</a>.

IOCTL_ACPI_EVAL_METHOD_EX can be used only at IRQL &lt; DISPATCH_LEVEL.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | acpiioct.h (include Acpiioct.h) |
| **IRQL** |  |

    ## See Also

        <dl>
<dt>
<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_EX</a>
</dt>
<dt>
<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_complex_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_COMPLEX_EX</a>
</dt>
<dt>
<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_simple_integer_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_SIMPLE_INTEGER_EX</a>
</dt>
<dt>
<a href="..\acpiioct\ns-acpiioct-_acpi_eval_input_buffer_simple_string_v1_ex.md">ACPI_EVAL_INPUT_BUFFER_SIMPLE_STRING_EX</a>
</dt>
<dt>
<a href="..\acpiioct\ns-acpiioct-_acpi_eval_output_buffer_v1.md">ACPI_EVAL_OUTPUT_BUFFER</a>
</dt>
<dt>
<a href="..\acpiioct\ni-acpiioct-ioctl_acpi_async_eval_method.md">IOCTL_ACPI_ASYNC_EVAL_METHOD</a>
</dt>
<dt>
<a href="..\acpiioct\ni-acpiioct-ioctl_acpi_async_eval_method_ex.md">IOCTL_ACPI_ASYNC_EVAL_METHOD_EX</a>
</dt>
<dt>
<a href="..\acpiioct\ni-acpiioct-ioctl_acpi_eval_method.md">IOCTL_ACPI_EVAL_METHOD</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [acpi\acpi]:%20IOCTL_ACPI_EVAL_METHOD_EX control code%20 RELEASE:%20(12/31/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>