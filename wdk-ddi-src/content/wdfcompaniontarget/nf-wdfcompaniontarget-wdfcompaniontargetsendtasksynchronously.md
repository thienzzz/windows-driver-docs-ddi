---
UID : NF:wdfcompaniontarget.WdfCompanionTargetSendTaskSynchronously
title : WdfCompanionTargetSendTaskSynchronously function
author : windows-driver-content
description : For internal use only.
old-location : wdf\wdfcompaniontargetsendtasksynchronously.htm
old-project : wdf
ms.assetid : d58a275a-aaaa-4159-ba00-6998b7a63434
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WdfCompanionTargetSendTaskSynchronously
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfcompaniontarget.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.23
req.umdf-ver : 
req.alt-api : WdfCompanionTargetSendTaskSynchronously
req.alt-loc : wdfcompaniontarget.h
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
req.typenames : WDF_TASK_SEND_OPTIONS_FLAGS
req.product : Windows 10 or later.
---


# WdfCompanionTargetSendTaskSynchronously function
For internal use only.

## Syntax

````
NTSTATUS WdfCompanionTargetSendTaskSynchronously(
  _In_     WDFCOMPANIONTARGET     CompanionTarget,
  _In_     USHORT                 TaskQueueIdentifier,
  _In_     ULONG                  TaskOperationCode,
  _In_opt_ PWDF_MEMORY_DESCRIPTOR InputBuffer,
  _In_opt_ PWDF_MEMORY_DESCRIPTOR OutputBuffer,
  _In_opt_ PWDF_TASK_SEND_OPTIONS TaskOptions,
  _Out_    PULONG_PTR             BytesReturned
);
````

## Parameters

`CompanionTarget`



`TaskQueueIdentifier`



`TaskOperationCode`



`InputBuffer`



`OutputBuffer`



`TaskOptions`



`BytesReturned`




## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** | 1.23 |
| **Minimum UMDF version** |  |
| **Header** | wdfcompaniontarget.h |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |