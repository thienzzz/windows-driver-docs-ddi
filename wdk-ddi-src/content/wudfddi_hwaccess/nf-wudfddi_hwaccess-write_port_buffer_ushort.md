---
UID : NF:wudfddi_hwaccess.WRITE_PORT_BUFFER_USHORT
title : WRITE_PORT_BUFFER_USHORT function
author : windows-driver-content
description : The WRITE_PORT_BUFFER_USHORT function writes a number of USHORT values from a buffer to the specified port address.
old-location : wdf\write_port_buffer_ushort.htm
old-project : wdf
ms.assetid : 04F51A7D-70D8-4844-973D-70B7A7797221
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WRITE_PORT_BUFFER_USHORT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wudfddi_hwaccess.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 1.11
req.alt-api : WRITE_PORT_BUFFER_USHORT
req.alt-loc : Wudfddi_hwaccess.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : Unavailable in UMDF 2.0 and later.
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : "*PUMDF_IO_TARGET_OPEN_PARAMS, UMDF_IO_TARGET_OPEN_PARAMS"
req.product : Windows 10 or later.
---


# WRITE_PORT_BUFFER_USHORT function
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>WRITE_PORT_BUFFER_USHORT</b> function writes a number of USHORT values from a buffer to the specified port address.

## Syntax

````
void WRITE_PORT_BUFFER_USHORT(
  _In_ IWDFDevice3 *pDevice,
  _In_ PUSHORT     Port,
  _In_ PUSHORT     Buffer,
  _In_ ULONG       Count 
);
````

## Parameters

`pDevice`

Specifies a pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfdevice3.md">IWDFDevice3</a> interface for the device object of the device to access.

`Port`

A pointer to the port, which must be a mapped memory range in I/O space.

`Buffer`

A pointer to a buffer from which an array of USHORT values is to be written.

`Count`

Specifies the number of USHORT values to be written to the buffer.


## Return Value

This function does not return a value.

## Remarks

For more information, see <a href="https://msdn.microsoft.com/A0640E60-B0DF-4CAD-B292-CC1875EF7F7D">Reading and Writing to Device Registers in UMDF 1.x Drivers</a>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** | 1.11 |
| **Header** | wudfddi_hwaccess.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |