---
UID : NF:ntddk.IoPropagateActivityIdToThread
title : IoPropagateActivityIdToThread function
author : windows-driver-content
description : The IoPropagateActivityIdToThread routine associates the activity ID from an IRP with the current thread.
old-location : kernel\iopropagateactivityidtothread.htm
old-project : kernel
ms.assetid : 8E824793-53DF-4573-81B0-6FE925CCB4C4
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : IoPropagateActivityIdToThread
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with  Windows 8.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoPropagateActivityIdToThread
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : Any level
req.typenames : WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---


# IoPropagateActivityIdToThread function
The <b>IoPropagateActivityIdToThread</b> routine associates the activity ID from an IRP with the current thread.

## Syntax

````
NTSTATUS IoPropagateActivityIdToThread(
  _In_  PIRP    Irp,
  _Out_ LPGUID  PropagatedId,
  _Out_ LPCGUID *OriginalId
);
````

## Parameters

`Irp`

The IRP whose ID will be propagated to the thread.

`PropagatedId`

A pointer to memory allocated by the caller to store the ID in the thread.

`OriginalId`




## Return Value

<b>IoPropagateActivityIdToThread</b> returns STATUS_SUCCESS if the call is successful. Possible error return values include the following.
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>The IRP does not have an ID associated with it.

## Remarks

This routine should be used by drivers that are tracing aware and are issuing I/O on a worker thread. Note that such drivers must call <a href="..\ntddk\nf-ntddk-ioclearactivityidthread.md">IoClearActivityIdThread</a> with the <i>OriginalId</i> before they return control from the thread, if the call was successful.

Drivers that use I/O work items do not need to call this routine because the I/O subsystem takes care of propagating activity IDs to threads in that case.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h) |
| **Library** |  |
| **IRQL** | Any level |
| **DDI compliance rules** |  |