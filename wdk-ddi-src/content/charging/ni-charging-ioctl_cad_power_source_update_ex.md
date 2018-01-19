---
UID : NI:charging.IOCTL_CAD_POWER_SOURCE_UPDATE_EX
title : IOCTL_CAD_POWER_SOURCE_UPDATE_EX
author : windows-driver-content
description : This IOCTL is for internal use only.
old-location : battery\ioctl_cad_power_source_update_ex.htm
old-project : battery
ms.assetid : 8D582EF9-B9D1-498B-AE20-337F3A33250C
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _POWERSOURCEID, POWERSOURCEID, *PPOWERSOURCEID
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : charging.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IOCTL_CAD_POWER_SOURCE_UPDATE_EX
req.alt-loc : charging.h
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
req.typenames : POWERSOURCEID, *PPOWERSOURCEID
---

# IOCTL_CAD_POWER_SOURCE_UPDATE_EX IOCTL
This IOCTL is for internal use only.

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer
<text></text>

### Input Buffer Length
<text></text>

### Output Buffer
<text></text>

### Output Buffer Length
<text></text>

### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code. 
For more information, see [XREF-LINK:NTSTATUS Values].


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | charging.h |
| **IRQL** |  |