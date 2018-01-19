---
UID : NC:wdm.GET_VIRTUAL_DEVICE_DATA
title : GET_VIRTUAL_DEVICE_DATA
author : windows-driver-content
description : The GetVirtualFunctionData routine reads data from the PCI Express (PCIe) configuration space of a virtual function (VF) on a device that supports the single root I/O virtualization (SR-IOV) interface.
old-location : pci\getvirtualfunctiondata.htm
old-project : PCI
ms.assetid : 2DE7417D-C616-4D1F-835D-29F477410F1E
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _WDI_TYPE_PMK_NAME, WDI_TYPE_PMK_NAME, *PWDI_TYPE_PMK_NAME
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : wdm.h
req.include-header : Wdm.h
req.target-type : Desktop
req.target-min-winverclnt : Supported in Windows Server 2012 and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : GetVirtualFunctionData
req.alt-loc : Wdm.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= APC_LEVEL
req.typenames : WDI_TYPE_PMK_NAME, *PWDI_TYPE_PMK_NAME
req.product : Windows 10 or later.
---


# GET_VIRTUAL_DEVICE_DATA function
The  <a href="https://msdn.microsoft.com/library/windows/hardware/hh451137">GetVirtualFunctionData</a> routine reads data from the PCI Express (PCIe) configuration space of a virtual function (VF) on a device that supports the single root I/O virtualization (SR-IOV) interface.

## Syntax

```
GET_VIRTUAL_DEVICE_DATA GetVirtualDeviceData;

ULONG GetVirtualDeviceData(
  PVOID Context,
  USHORT VirtualFunction,
  PVOID Buffer,
  ULONG Offset,
  ULONG Length
)
{...}
```

## Parameters

`Context`

A pointer to interface-specific context information. The caller passes the value that is passed as the <b>Context</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406642">PCI_VIRTUALIZATION_INTERFACE</a> structure for the interface.

`VirtualFunction`

A zero-based value that specifies the VF on the device from which data is to be read.

`Buffer`

A pointer to the buffer that contains the configuration information read from the PCIe configuration space of the VF.

`Offset`

The offset into the PCIe configuration space data of the VF. This member specifies where this read operation begins.

`Length`

The length, in bytes, of the data to be read.


## Return Value

The 
      <a href="https://msdn.microsoft.com/library/windows/hardware/hh451137">GetVirtualFunctionData</a> routine returns the length, in bytes, of the PCIe configuration data that was read after a successful read operation. If the read operation is unsuccessful, the routine returns zero.

## Remarks

The <a href="https://msdn.microsoft.com/library/windows/hardware/hh451137">GetVirtualFunctionData</a> routine resembles the <a href="..\wdm\nc-wdm-get_set_device_data.md">GetBusData</a> routine, except that it reads PCIe configuration data from a VF instead of from a device's physical function (PF).

The <a href="https://msdn.microsoft.com/library/windows/hardware/hh451137">GetVirtualFunctionData</a> routine is provided by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451143">GUID_PCI_VIRTUALIZATION_INTERFACE</a> interface. The <a href="..\wdm\nc-wdm-get_set_device_data.md">GetBusData</a> routine is provided by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546561">GUID_BUS_INTERFACE_STANDARD</a> interface.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt><b></b></dt>
<dt>
<a href="..\wdm\nc-wdm-get_set_device_data.md">GetBusData</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546561">GUID_BUS_INTERFACE_STANDARD</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451143">GUID_PCI_VIRTUALIZATION_INTERFACE</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406642">PCI_VIRTUALIZATION_INTERFACE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\pci]:%20GET_VIRTUAL_DEVICE_DATA routine%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>