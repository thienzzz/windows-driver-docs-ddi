---
UID : NC:iddcx.EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP
title : EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP
author : windows-driver-content
description : EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP is called by the OS to set a gamma ramp on the specified monitor.
old-location : display\evt_idd_cx_monitor_set_gamma_ramp.htm
old-project : display
ms.assetid : 3e0828ee-307a-48fd-a8ea-b469ac6214d0
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : WcsTranslateColors
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : iddcx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PFN_IDD_CX_MONITOR_SET_GAMMA_RAMP
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
req.irql : _requires_same_
req.typenames : WCS_PROFILE_MANAGEMENT_SCOPE
---


# EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP function
<b>EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP</b> is called by the OS to set a gamma ramp on the specified monitor.

## Syntax

```
EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP EvtIddCxMonitorSetGammaRamp;

_IRQL_requires_same_ NTSTATUS EvtIddCxMonitorSetGammaRamp(
  IDDCX_MONITOR MonitorObject,
  const IDARG_IN_SET_GAMMARAMP * pInArgs
)
{...}
```

## Parameters

`MonitorObject`

A handle by the OS to identify the monitor to set a gamma ramp for.

`pInArgs`

Input arguments used by <b>EVT_IDD_CX_MONITOR_SET_GAMMA_RAMP</b>.


## Return Value

(NTSTATUS) If the operation is successful, the callback function must return STATUS_SUCCESS, or another status value for which NT_SUCCESS(status) equals TRUE. Otherwise, an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | iddcx.h |
| **Library** |  |
| **IRQL** | _requires_same_ |
| **DDI compliance rules** |  |