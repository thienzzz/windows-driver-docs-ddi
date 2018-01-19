---
UID : NF:iddcx.IddCxMonitorUpdateModes
title : IddCxMonitorUpdateModes function
author : windows-driver-content
description : An OS callback function the driver calls to update the mode list.
old-location : display\iddcxmonitorupdatemodes.htm
old-project : display
ms.assetid : 0f05931a-2327-454a-9ba7-da02cb2f13d9
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : IddCxMonitorUpdateModes
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : iddcx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IddCxMonitorUpdateModes
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
req.irql : _Must_inspect_result_
req.typenames : 
---


# IddCxMonitorUpdateModes function
An OS callback function the driver calls to update the mode list

## Syntax

````
NTSTATUS IddCxMonitorUpdateModes(
  _In_       IDDCX_MONITOR         MonitorObject,
  _In_ const IDARG_IN_UPDATEMODES* pInArgs
);
````

## Parameters

`MonitorObject`

The monitor object being updated

`pInArgs`

Input arguments of function


## Return Value

(NTSTATUS) The method returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method may return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | iddcx.h |
| **Library** |  |
| **IRQL** | _Must_inspect_result_ |
| **DDI compliance rules** |  |