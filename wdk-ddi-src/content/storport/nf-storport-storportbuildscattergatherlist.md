---
UID : NF:storport.StorPortBuildScatterGatherList
title : StorPortBuildScatterGatherList function
author : windows-driver-content
description : The StorPortBuildScatterGatherList routine creates a scatter/gather list for the specified data buffer.
old-location : storage\storportbuildscattergatherlist.htm
old-project : storage
ms.assetid : cdea67aa-14fa-45c1-8af0-8db48042b1b2
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortBuildScatterGatherList
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortBuildScatterGatherList
req.alt-loc : storport.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : DISPATCH_LEVEL
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortBuildScatterGatherList function
The <b>StorPortBuildScatterGatherList</b> routine creates a scatter/gather list for the specified data buffer.

## Syntax

````
ULONG StorPortBuildScatterGatherList(
  _In_    PVOID                        HwDeviceExtension,
  _In_    PVOID                        Mdl,
  _In_    PVOID                        CurrentVa,
  _In_    ULONG                        Length,
  _In_    PPOST_SCATTER_GATHER_EXECUTE ExecutionRoutine,
  _In_    PVOID                        Context,
  _In_    BOOLEAN                      WriteToDevice,
  _Inout_ PVOID                        ScatterGatherBuffer,
  _In_    ULONG                        ScatterGatherBufferLength
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension for the host bus adapter (HBA).

`Mdl`

A pointer to a memory descriptor list (MDL) that describes the memory pages associated with the data buffer.

`CurrentVa`

The virtual address of the data buffer.

`Length`

The length, in bytes, of the data buffer.

`ExecutionRoutine`

A pointer to a miniport driver-supplied <i>ExecutionRoutine</i>. The Storport driver calls this routine after creating the scatter/gather list. The miniport driver should perform all operations that make use of the scatter/gather list inside the execution routine, not in the code that follows the call to the <b>StorPortBuildScatterGatherList</b> routine.

An <i>ExecutionRoutine</i> is declared as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>VOID
ExecutionRoutine (
    IN PVOID  *DeviceObject,
    IN PVOID  *Irp,
    IN PSTOR_SCATTER_GATHER_LIST  ScatterGather,
    IN PVOID  Context
    );</pre>
</td>
</tr>
</table></span></div>

`Context`

The context value specified in the <b>StorPortBuildScatterGatherList</b> function's <i>Context</i> parameter.

</dd>
</dl>
The Storport driver calls a miniport driver's <i>ExecutionRoutine</i> at IRQL = DISPATCH_LEVEL.

`WriteToDevice`

A value that indicates the direction of the DMA transfer. A value of <b>TRUE</b> indicates a transfer that is from the data buffer to the device, and a value of <b>FALSE</b> indicates a transfer that is from the device to the data buffer.

`ScatterGatherBuffer`

A pointer to a miniport-supplied buffer that receives the scatter/gather list. A miniport driver can allocate memory for this buffer by calling the <a href="..\storport\nf-storport-storportallocatepool.md">StorPortAllocatePool</a> routine.

`ScatterGatherBufferLength`

The size, in bytes, of the buffer pointed to by the <i>ScatterGatherBuffer</i> parameter.


## Return Value

<b>StorPortBuildScatterGatherList</b> returns one of the following values:
<dl>
<dt><b>STOR_STATUS_NOT_IMPLEMENTED</b></dt>
</dl>This function is not implemented on the active operating system.
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>Indicates that the routine created the scatter/gather list successfully.
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl>The <i>HwDeviceExtension</i> passed was <b>NULL</b>.
<dl>
<dt><b>STOR_STATUS_INVALID_IRQL</b></dt>
</dl>The call was made at an invalid IRQL.
<dl>
<dt><b>STOR_STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>The system has insufficient map registers available for the transfer.
<dl>
<dt><b>STOR_STATUS_BUFFER_TOO_SMALL </b></dt>
</dl>The Length parameter is too big to fit within the buffer.

## Remarks

The miniport driver calls <a href="..\storport\nf-storport-storportputscattergatherlist.md">StorPortPutScatterGatherList</a> to release the resources that <b>StorPortBuildScatterGatherList</b> allocated while constructing the scatter/gather list. 

The miniport driver must call <a href="..\storport\nf-storport-storportputscattergatherlist.md">StorPortPutScatterGatherList</a> before freeing or reusing the memory it allocated for the scatter/gather list.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** | DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\storport\nf-storport-storportallocatepool.md">StorPortAllocatePool</a>
</dt>
<dt>
<a href="..\storport\nf-storport-storportputscattergatherlist.md">StorPortPutScatterGatherList</a>
</dt>
<dt>
<a href="..\storport\ns-storport-_stor_scatter_gather_list.md">STOR_SCATTER_GATHER_LIST</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortBuildScatterGatherList routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>