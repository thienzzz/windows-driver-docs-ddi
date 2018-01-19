---
UID : NC:d3dkmddi.DXGKDDI_MONITORDESCRIPTORSET_GETNUMDESCRIPTORS
title : DXGKDDI_MONITORDESCRIPTORSET_GETNUMDESCRIPTORS
author : windows-driver-content
description : The pfnGetNumDescriptors function returns the number of descriptors in a monitor descriptor set.
old-location : display\dxgk_monitordescriptorset_interface_pfngetnumdescriptors.htm
old-project : display
ms.assetid : 7bfcef0b-1371-4e3b-b5dc-c4c548625c8f
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DD_MULTISAMPLEQUALITYLEVELSDATA, DD_MULTISAMPLEQUALITYLEVELSDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnGetNumDescriptors
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


# DXGKDDI_MONITORDESCRIPTORSET_GETNUMDESCRIPTORS callback function
The <b>pfnGetNumDescriptors</b> function returns the number of descriptors in a monitor descriptor set.

## Syntax

```
DXGKDDI_MONITORDESCRIPTORSET_GETNUMDESCRIPTORS DxgkddiMonitordescriptorsetGetnumdescriptors;

NTSTATUS DxgkddiMonitordescriptorsetGetnumdescriptors(
  IN_CONST_D3DKMDT_HMONITORDESCRIPTORSET hMonitorDescriptorSet,
  OUT_PSIZE_T_CONST pNumMonitorDescriptors
)
{...}
```

## Parameters

`hMonitorDescriptorSet`

[in] A handle to a monitor descriptor set object. The display miniport driver previously obtained this handle by calling the <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_monitor_getmonitordescriptorset.md">pfnGetMonitorDescriptorSet</a> function of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568433">Monitor interface</a>.

`pNumMonitorDescriptors`

[out] A SIZE_T-typed variable that receives the number of descriptors in the set.


## Return Value

The <b>pfnGetNumDescriptors</b> function returns one of the following values.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The function succeeded.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>An invalid parameter was supplied.
<dl>
<dt><b>STATUS_GRAPHICS_INVALID_MONITOR_DESCRIPTORSET</b></dt>
</dl>The handle supplied in <i>hMonitorDescriptorSet</i> was invalid.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |