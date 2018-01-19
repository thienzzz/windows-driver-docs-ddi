---
UID : NC:dispmprt.DXGKCB_SYNCHRONIZE_EXECUTION
title : DXGKCB_SYNCHRONIZE_EXECUTION
author : windows-driver-content
description : The DxgkCbSynchronizeExecution function synchronizes a specified function, implemented by the display miniport driver, with the display miniport driver's DxgkDdiInterruptRoutine function.
old-location : display\dxgkcbsynchronizeexecution.htm
old-project : display
ms.assetid : 9c659319-d0a5-43a7-b9a9-9fad18397a09
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _SYMBOL_INFO_EX, *PSYMBOL_INFO_EX, SYMBOL_INFO_EX
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : dispmprt.h
req.include-header : Dispmprt.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DxgkCbSynchronizeExecution
req.alt-loc : dispmprt.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : "*PSYMBOL_INFO_EX, SYMBOL_INFO_EX"
---


# DXGKCB_SYNCHRONIZE_EXECUTION callback function
The <b>DxgkCbSynchronizeExecution</b> function synchronizes a specified function, implemented by the display miniport driver, with the display miniport driver's <a href="..\dispmprt\nc-dispmprt-dxgkddi_interrupt_routine.md">DxgkDdiInterruptRoutine</a> function.

## Syntax

```
DXGKCB_SYNCHRONIZE_EXECUTION DxgkcbSynchronizeExecution;

NTSTATUS DxgkcbSynchronizeExecution(
  HANDLE DeviceHandle,
  PKSYNCHRONIZE_ROUTINE SynchronizeRoutine,
  PVOID Context,
  ULONG MessageNumber,
  PBOOLEAN ReturnValue
)
{...}
```

## Parameters

`DeviceHandle`

A handle that represents a display adapter. The display miniport driver previously obtained this handle in the <b>DeviceHandle</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560942">DXGKRNL_INTERFACE</a> structure that was passed to <a href="..\dispmprt\nc-dispmprt-dxgkddi_start_device.md">DxgkDdiStartDevice</a>.

`SynchronizeRoutine`

A pointer to a function, implemented by the display miniport driver, that will be synchronized with <i>DxgkDdiInterruptRoutine</i>. The function must conform to the following prototype:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BOOLEAN SynchronizeRoutine(PVOID Context);</pre>
</td>
</tr>
</table></span></div>

`Context`

A pointer to a context block, created by the display miniport driver, that will be passed to <i>SynchronizeRoutine</i>.

`MessageNumber`

The number of the interrupt message with which <i>SynchronizeRoutine</i> will be synchronized. If the interrupt is line-based, this parameter must be zero.

`ReturnValue`

A pointer to a Boolean variable that receives the return value of <i>SynchronizeRoutine</i>.


## Return Value

<b>DxgkCbSynchronizeExecution</b> returns one of the following values:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The function succeeded.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>One of the parameters is invalid.
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>The function was unable to synchronize execution, possibly because the interrupt had not been connected yet.

 

The following code example shows a submission thread that notifies the GPU scheduler about the completion of packets from the software queue.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dispmprt.h (include Dispmprt.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\dispmprt\nc-dispmprt-dxgkddi_interrupt_routine.md">DxgkDdiInterruptRoutine</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-kesynchronizeexecution.md">KeSynchronizeExecution</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGKCB_SYNCHRONIZE_EXECUTION callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>