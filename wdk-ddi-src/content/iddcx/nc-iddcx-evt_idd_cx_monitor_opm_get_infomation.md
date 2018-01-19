---
UID : NC:iddcx.EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION
title : EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION
author : windows-driver-content
description : EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION is called by the OS to get OPM information.
old-location : display\evt_idd_cx_monitor_opm_get_infomation.htm
old-project : display
ms.assetid : b616a105-3c4b-42b7-8352-a1f35479572e
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
req.alt-api : PFN_IDD_CX_MONITOR_OPM_GET_INFOMATION
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


# EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION function
<b>EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION</b> is called by the OS to get OPM information.

## Syntax

```
EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION EvtIddCxMonitorOpmGetInfomation;

_IRQL_requires_same_ NTSTATUS EvtIddCxMonitorOpmGetInfomation(
  IDDCX_OPMCTX OpmCxtObject,
  const IDARG_IN_OPM_GET_INFOMATION * pInArgs,
  IDARG_OUT_OPM_GET_INFOMATION * pOutArgs
)
{...}
```

## Parameters

`OpmCxtObject`

The object for the OPM context that information will be gotten from.

`pInArgs`

Input arguments used by <b>EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION</b>.

`pOutArgs`

Output arguments returned by <b>EVT_IDD_CX_MONITOR_OPM_GET_INFOMATION</b>.


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