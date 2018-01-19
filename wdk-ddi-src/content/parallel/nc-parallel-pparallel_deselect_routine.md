---
UID : NC:parallel.PPARALLEL_DESELECT_ROUTINE
title : PPARALLEL_DESELECT_ROUTINE
author : windows-driver-content
description : The PPARALLEL_DESELECT_ROUTINE-typed callback routine deselects either an IEEE 1284.3 daisy chain device or an IEEE 1284 end-of-chain device that is attached to a parallel port.
old-location : parports\pparallel_deselect_routine.htm
old-project : parports
ms.assetid : 91182ed5-e444-41a7-b6fc-f14d0407f089
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : RegisterOpRegionHandler
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : parallel.h
req.include-header : Parallel.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : (*PPARALLEL_DESELECT_ROUTINE)
req.alt-loc : parallel.h
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
req.typenames : "*LPRILGBATOKEN, RILGBATOKEN"
---


# PPARALLEL_DESELECT_ROUTINE callback function
The <i>PPARALLEL_DESELECT_ROUTINE</i>-typed callback routine deselects either an IEEE 1284.3 daisy chain device or an IEEE 1284 end-of-chain device that is attached to a parallel port. The system-supplied function driver for parallel ports supplies this routine.

## Syntax

```
PPARALLEL_DESELECT_ROUTINE PparallelDeselectRoutine;

NTSTATUS PparallelDeselectRoutine(
  PVOID DeselectContext,
  PVOID DeselectCommand
)
{...}
```

## Parameters

`DeselectContext`

Pointer to the device extension of a functional device object (<a href="wdkgloss.f#wdkgloss.fdo#wdkgloss.fdo"><i>FDO</i></a>) that represents a parallel port.

`DeselectCommand`

Pointer to a PARALLEL_1284_COMMAND structure. The caller specifies the following members:


## Return Value

<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The device was deselected.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>The specified device ID is invalid.
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>The system-supplied function driver for parallel ports could not deselect the device.

## Remarks

To obtain a pointer to the system-supplied <i>PPARALLEL_DESELECT_ROUTINE</i> callback, a kernel-mode driver uses an <a href="..\parallel\ni-parallel-ioctl_internal_get_parallel_pnp_info.md">IOCTL_INTERNAL_GET_PARALLEL_PNP_INFO</a> request, which returns a <a href="..\parallel\ns-parallel-_parallel_pnp_information.md">PARALLEL_PNP_INFORMATION</a> structure. The <b>DeselectDevice</b> member of the PARALLEL_PNP_INFORMATION structure is a pointer to this callback.

A kernel-mode driver can use an <a href="..\parallel\ni-parallel-ioctl_internal_deselect_device.md">IOCTL_INTERNAL_DESELECT_DEVICE</a> request or the <i>PPARALLEL_CLEAR_CHIP_MODE</i> callback to deselect a device on a parallel port represented by a parallel port. To deselect a device, a caller should have the parallel port allocated. If the caller does not set the PAR_HAVE_PORT_KEEP_PORT flag, the system-supplied function driver for parallel ports frees the parallel port after deselecting the device.

For more information, see <a href="https://msdn.microsoft.com/1a3ac1b1-9180-4b71-8740-70c6fbe9a885">Selecting and Deselecting an IEEE 1284 Device Attached to a ParallelPort</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | parallel.h (include Parallel.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\parallel\ni-parallel-ioctl_internal_deselect_device.md">IOCTL_INTERNAL_DESELECT_DEVICE</a>
</dt>
<dt>
<a href="..\parallel\ni-parallel-ioctl_internal_select_device.md">IOCTL_INTERNAL_SELECT_DEVICE</a>
</dt>
<dt>
<a href="..\parallel\ns-parallel-_parallel_pnp_information.md">PARALLEL_PNP_INFORMATION</a>
</dt>
<dt>
<a href="..\parallel\nc-parallel-pparallel_try_select_routine.md">PPARALLEL_TRY_SELECT_ROUTINE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [parports\parports]:%20PPARALLEL_DESELECT_ROUTINE callback function%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>