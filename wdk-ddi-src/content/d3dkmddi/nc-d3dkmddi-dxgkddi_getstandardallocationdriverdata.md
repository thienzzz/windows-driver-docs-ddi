---
UID : NC:d3dkmddi.DXGKDDI_GETSTANDARDALLOCATIONDRIVERDATA
title : DXGKDDI_GETSTANDARDALLOCATIONDRIVERDATA
author : windows-driver-content
description : The DxgkDdiGetStandardAllocationDriverData function returns a description of a standard allocation type.
old-location : display\dxgkddigetstandardallocationdriverdata.htm
old-project : display
ms.assetid : 38a9859f-ed9f-41a5-9bf1-c734480499ea
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DD_MULTISAMPLEQUALITYLEVELSDATA, DD_MULTISAMPLEQUALITYLEVELSDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dkmddi.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DxgkDdiGetStandardAllocationDriverData
req.alt-loc : d3dkmddi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : DD_MULTISAMPLEQUALITYLEVELSDATA
---


# DXGKDDI_GETSTANDARDALLOCATIONDRIVERDATA function
The <i>DxgkDdiGetStandardAllocationDriverData</i> function returns a description of a standard allocation type.

## Syntax

```
DXGKDDI_GETSTANDARDALLOCATIONDRIVERDATA DxgkddiGetstandardallocationdriverdata;

NTSTATUS DxgkddiGetstandardallocationdriverdata(
  IN_CONST_HANDLE hAdapter,
  INOUT_PDXGKARG_GETSTANDARDALLOCATIONDRIVERDATA pGetStandardAllocationDriverData
)
{...}
```

## Parameters

`hAdapter`

[in] A handle to a context block that is associated with a display adapter. The display miniport driver previously provided this handle to the Microsoft DirectX graphics kernel subsystem in the <i>MiniportDeviceContext</i> output parameter of the <a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a> function.

`pGetStandardAllocationDriverData`

[in/out] A pointer to a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_getstandardallocationdriverdata.md">DXGKARG_GETSTANDARDALLOCATIONDRIVERDATA</a> structure that describes a standard allocation.


## Return Value

<i>DxgkDdiGetStandardAllocationDriverData</i> returns one of the following values:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl><i>DxgkDdiGetStandardAllocationDriverData</i> successfully returned a description of the standard allocation type.
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl><i>DxgkDdiGetStandardAllocationDriverData</i> could not allocate memory that was required for it to complete.

## Remarks

<i>Standard allocation types</i> are allocations that must be created in kernel mode without communication from the user-mode display driver. The DirectX graphics kernel subsystem calls the <i>DxgkDdiGetStandardAllocationDriverData</i> function to generate a description of the standard allocation type that the <i>pGetStandardAllocationDriverData</i> parameter specifies. The display miniport driver returns the description of the allocation type in the <b>pAllocationPrivateDriverData</b> and <b>pResourcePrivateDriverData</b> members of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_getstandardallocationdriverdata.md">DXGKARG_GETSTANDARDALLOCATIONDRIVERDATA</a> structure that the <i>pGetStandardAllocationDriverData</i> parameter points to. The DirectX graphics kernel subsystem subsequently passes the description to the <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createallocation.md">DxgkDdiCreateAllocation</a> function to actually create the allocation.

Beginning with Windows 7, if a display miniport driver processes a call to the <i>DxgkDdiGetStandardAllocationDriverData</i> function to create allocations for GDI hardware acceleration, the driver should set the pitch of the allocation for CPU visible allocations, <i>pGetStandardAllocationDriverData-&gt;</i><b>pCreateGdiSurfaceData</b><i>-&gt;</i><b>Pitch</b>.

<i>DxgkDdiGetStandardAllocationDriverData</i> should be made pageable.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_getstandardallocationdriverdata.md">DXGKARG_GETSTANDARDALLOCATIONDRIVERDATA</a>
</dt>
<dt>
<a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createallocation.md">DxgkDdiCreateAllocation</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGKDDI_GETSTANDARDALLOCATIONDRIVERDATA callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>