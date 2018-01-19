---
UID : NE:wdfcompanion._WDF_TASK_QUEUE_DISPATCH_TYPE
title : _WDF_TASK_QUEUE_DISPATCH_TYPE
author : windows-driver-content
description : For internal use only.
old-location : wdf\wdf_task_queue_dispatch_type.htm
old-project : wdf
ms.assetid : 27cc4067-33de-4f2d-abad-05c73c875458
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDF_TASK_QUEUE_DISPATCH_TYPE, WDF_TASK_QUEUE_DISPATCH_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wdfcompanion.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 2.23
req.alt-api : WDF_TASK_QUEUE_DISPATCH_TYPE
req.alt-loc : wdfcompanion.h
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
req.typenames : WDF_TASK_QUEUE_DISPATCH_TYPE
req.product : Windows 10 or later.
---

# _WDF_TASK_QUEUE_DISPATCH_TYPE Enumeration
For internal use only.

## Syntax
````
typedef enum _WDF_TASK_QUEUE_DISPATCH_TYPE { 
  WdfTaskQueueDispatchInvalid     = 0,
  WdfTaskQueueDispatchSequential,
  WdfTaskQueueDispatchParallel,
  WdfTaskQueueDispatchMax
} WDF_TASK_QUEUE_DISPATCH_TYPE;
````

## Constants

<table>

<tr>
<td>WdfTaskQueueDispatchInvalid</td>
<td></td>
</tr>

<tr>
<td>WdfTaskQueueDispatchMax</td>
<td></td>
</tr>

<tr>
<td>WdfTaskQueueDispatchParallel</td>
<td></td>
</tr>

<tr>
<td>WdfTaskQueueDispatchSequential</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** | 2.23 |
| **Header** | wdfcompanion.h |