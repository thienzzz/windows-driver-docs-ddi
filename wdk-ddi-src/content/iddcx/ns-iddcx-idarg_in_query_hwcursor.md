---
UID : NS:iddcx.IDARG_IN_QUERY_HWCURSOR
title : IDARG_IN_QUERY_HWCURSOR
author : windows-driver-content
description : Gives information about the cursor associated with the monitor.
old-location : display\idarg_in_query_hwcursor.htm
old-project : display
ms.assetid : 293364D0-0614-4780-B5E5-1115F084A8C6
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : IDARG_IN_QUERY_HWCURSOR,
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : iddcx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDARG_IN_QUERY_HWCURSOR
req.alt-loc : iddcx.h
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
req.typenames : 
---

# IDARG_IN_QUERY_HWCURSOR structure
Gives information about the cursor associated with the monitor.

## Syntax
````
typedef struct _IDARG_IN_QUERY_HWCURSOR {
  IDDCX_MONITOR_DESCRIPTION                                   MonitorDescription;
  UINT                                                        TargetModeBufferInputCount;
  _Field_size_(TargetModeBufferInputCount) IDDCX_TARGET_MODE* pTargetModes;
} IDARG_IN_QUERY_HWCURSOR, *PIDARG_IN_QUERY_HWCURSOR;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | iddcx.h |