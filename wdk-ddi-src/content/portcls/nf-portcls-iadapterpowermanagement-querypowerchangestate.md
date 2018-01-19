---
UID : NF:portcls.IAdapterPowerManagement.QueryPowerChangeState
title : IAdapterPowerManagement::QueryPowerChangeState method
author : windows-driver-content
description : The QueryPowerChangeState method is called by PortCls in response to the receipt of an IRP_MN_QUERY_POWER power IRP.
old-location : audio\iadapterpowermanagement_querypowerchangestate.htm
old-project : audio
ms.assetid : 32cd29c3-e8da-4119-84a4-3ce4daed528e
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : IAdapterPowerManagement, IAdapterPowerManagement::QueryPowerChangeState, QueryPowerChangeState
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : portcls.h
req.include-header : Portcls.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IAdapterPowerManagement.QueryPowerChangeState
req.alt-loc : portcls.h
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
req.typenames : PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---


# QueryPowerChangeState method
The <code>QueryPowerChangeState</code> method is called by PortCls in response to the receipt of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff551699">IRP_MN_QUERY_POWER</a> power IRP.

## Syntax

````
NTSTATUS QueryPowerChangeState(
  [in] POWER_STATE NewStateQuery
);
````

## Parameters

`NewStateQuery`

Specifies the new power state that is being requested for the device. This parameter is a union of type POWER_STATE. The new power state (<i>NewStateQuery</i>.<b>DeviceState</b>) can be one of the DEVICE_POWER_STATE enumeration values listed in <a href="https://msdn.microsoft.com/library/windows/hardware/ff536488">IAdapterPowerManagement::PowerChangeState</a>.


## Return Value

<code>QueryPowerChangeState</code> returns STATUS_SUCCESS if call was successful. Otherwise, the method returns an appropriate error code.

## Remarks

PortCls calls the <code>QueryPowerChangeState</code> method on behalf of the system to query the adapter driver for acceptability of a potential device power-state change. The driver can deny the power state change by returning a value other than STATUS_SUCCESS. A call to <code>QueryPowerStateChange</code> is not guaranteed to occur prior to all <b>PowerChangeState</b> calls.

The code for this method must reside in paged memory.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | portcls.h (include Portcls.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\portcls\nn-portcls-iadapterpowermanagement.md">IAdapterPowerManagement</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551699">IRP_MN_QUERY_POWER</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536488">IAdapterPowerManagement::PowerChangeState</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20IAdapterPowerManagement::QueryPowerChangeState method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>