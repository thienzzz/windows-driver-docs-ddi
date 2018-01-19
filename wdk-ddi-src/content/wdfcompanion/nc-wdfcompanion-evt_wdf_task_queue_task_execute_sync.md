---
UID : NC:wdfcompanion.EVT_WDF_TASK_QUEUE_TASK_EXECUTE_SYNC
title : EVT_WDF_TASK_QUEUE_TASK_EXECUTE_SYNC
author : windows-driver-content
description : For internal use only.
old-location : wdf\evt_wdf_task_queue_task_execute_sync.htm
old-project : wdf
ms.assetid : c45d1873-fb29-49ee-b99b-09861478ac89
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WDF_COMMON_BUFFER_CONFIG, *PWDF_COMMON_BUFFER_CONFIG, WDF_COMMON_BUFFER_CONFIG
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : wdfcompanion.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 2.23
req.alt-api : EVT_WDF_TASK_QUEUE_TASK_EXECUTE_SYNC
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
req.typenames : "*PWDF_COMMON_BUFFER_CONFIG, WDF_COMMON_BUFFER_CONFIG"
req.product : Windows 10 or later.
---


# EVT_WDF_TASK_QUEUE_TASK_EXECUTE_SYNC function
For internal use only.

## Syntax

```
EVT_WDF_TASK_QUEUE_TASK_EXECUTE_SYNC EvtWdfTaskQueueTaskExecuteSync;

NTSTATUS EvtWdfTaskQueueTaskExecuteSync(
  WDFTASKQUEUE Queue,
  PVOID InputBuffer,
  PVOID OutputBuffer,
  size_t InputBufferLength,
  size_t OutputBufferLength,
  size_t * BytesWritten,
  ULONG TaskOperationCode
)
{...}
```

## Parameters

`Queue`



`InputBuffer`



`OutputBuffer`



`InputBufferLength`



`OutputBufferLength`



`BytesWritten`



`TaskOperationCode`




## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** | 2.23 |
| **Header** | wdfcompanion.h |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |