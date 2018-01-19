---
UID : NF:ntifs.RtlCaptureStackBackTrace
title : RtlCaptureStackBackTrace function
author : windows-driver-content
description : The RtlCaptureStackBackTrace routine captures a stack back trace by walking up the stack and recording the information for each frame.
old-location : ifsk\rtlcapturestackbacktrace.htm
old-project : ifsk
ms.assetid : e4ad1eac-1788-4dfe-9444-f40e0de156c4
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RtlCaptureStackBackTrace
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h, FltKernel.h
req.target-type : Universal
req.target-min-winverclnt : Available in starting with Windows XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlCaptureStackBackTrace
req.alt-loc : NtDll.dll,NtosKrnl.exe,API-MS-Win-Core-RTLSupport-l1-1-0.dll,API-MS-Win-Core-RTLSupport-l1-2-0.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib; OneCoreUAP.lib on Windows 10
req.dll : NtDll.dll (user mode); NtosKrnl.exe (kernel mode)
req.irql : <= DISPATCH_LEVEL
req.typenames : TOKEN_TYPE
---


# RtlCaptureStackBackTrace function
The <b>RtlCaptureStackBackTrace</b> routine captures a stack back trace by walking up the stack and recording the information for each frame.

## Syntax

````
USHORT RtlCaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
````

## Parameters

`FramesToSkip`

The number of frames to skip from the start of the back trace.

`FramesToCapture`

The number of frames to be captured.

`BackTrace`

An array of pointers captured from the current stack trace.

`BackTraceHash`

An optional value that can be used to organize hash tables. If this parameter is <b>NULL</b>, no hash value is computed.

This value is calculated based on the values of the pointers returned in the <i>BackTrace</i> array. Two identical stack traces will generate identical hash values.


## Return Value

The number of captured frames.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h, FltKernel.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |