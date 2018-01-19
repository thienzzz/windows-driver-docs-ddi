---
UID : NF:storport.StorPortGetGroupAffinity
title : StorPortGetGroupAffinity function
author : windows-driver-content
description : The StorPortGetGroupAffinity routine constructs a mask of the active processors in a requested group.
old-location : storage\storportgetgroupaffinity.htm
old-project : storage
ms.assetid : eec0c985-fb59-4190-afb8-5eb62ac1edea
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortGetGroupAffinity
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : Available in Windows 7 and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortGetGroupAffinity
req.alt-loc : storport.h
req.ddi-compliance : StorPortIrql
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortGetGroupAffinity function
The <b>StorPortGetGroupAffinity</b> routine constructs a mask of the active processors in a requested group.

## Syntax

````
ULONG StorPortGetGroupAffinity(
  _In_  PVOID      HwDeviceExtension,
  _In_  USHORT     GroupNumber,
  _Out_ PKAFFINITY GroupAffinityMask
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension for the host bus adapter (HBA).

`GroupNumber`

The group from which to return the processor mask.

`GroupAffinityMask`

A pointer to a variable that holds the affinity mask of the given group.


## Return Value

The <b>StorPortGetGroupAffinity</b> routine returns one of the following status codes:
<dl>
<dt><b>STOR_STATUS_NOT_IMPLEMENTED</b></dt>
</dl>This function is not implemented on the active operating system.
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>The operation was successful.
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl>The operation fails with this return value if one or more of the parameters are invalid, for example, if <i>GroupAffinityMask</i> is set to <b>NULL</b>.
<dl>
<dt><b>STOR_STATUS_UNSUCCESSFUL</b></dt>
</dl>The operation fails with this return value if one or more of the parameters are invalid, for example, if <i>GroupNumber</i> is set to a value greater than the active group count.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** | StorPortIrql |