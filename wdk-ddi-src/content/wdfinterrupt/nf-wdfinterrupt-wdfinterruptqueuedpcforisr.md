---
UID : NF:wdfinterrupt.WdfInterruptQueueDpcForIsr
title : WdfInterruptQueueDpcForIsr function
author : windows-driver-content
description : The WdfInterruptQueueDpcForIsr method queues a framework interrupt object's EvtInterruptDpc callback function for execution.
old-location : wdf\wdfinterruptqueuedpcforisr.htm
old-project : wdf
ms.assetid : ba9a292d-12c8-41b5-bddb-7c8ebf4fdc48
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WdfInterruptQueueDpcForIsr
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfinterrupt.h
req.include-header : Wdf.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.0
req.umdf-ver : 2.0
req.alt-api : WdfInterruptQueueDpcForIsr
req.alt-loc : Wdf01000.sys,Wdf01000.sys.dll,WUDFx02000.dll,WUDFx02000.dll.dll
req.ddi-compliance : DriverCreate
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Wdf01000.sys (KMDF); WUDFx02000.dll (UMDF)
req.dll : 
req.irql : <=DIRQL
req.typenames : WDF_INTERRUPT_PRIORITY, *PWDF_INTERRUPT_PRIORITY
req.product : Windows 10 or later.
---


# WdfInterruptQueueDpcForIsr function
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WdfInterruptQueueDpcForIsr</b> method queues a framework interrupt object's <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_dpc.md">EvtInterruptDpc</a> callback function for execution.

## Syntax

````
BOOLEAN WdfInterruptQueueDpcForIsr(
  _In_ WDFINTERRUPT Interrupt
);
````

## Parameters

`Interrupt`

A handle to a framework interrupt object.


## Return Value

<b>WdfInterruptQueueDpcForIsr</b> returns <b>TRUE</b> if it successfully queues the interrupt object's <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_dpc.md">EvtInterruptDpc</a> callback function. The method returns <b>FALSE</b> if the callback function was previously queued and has not executed.

A bug check occurs if the driver supplies an invalid object handle.

## Remarks

Drivers typically call <b>WdfInterruptQueueDpcForIsr</b> from within an <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_isr.md">EvtInterruptIsr</a> callback function.

An interrupt object's <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_dpc.md">EvtInterruptDpc</a> callback function can be queued only once before it executes. Therefore, if a call to <b>WdfInterruptQueueDpcForIsr</b> succeeds, subsequent calls will return <b>FALSE</b> until the framework dequeues and executes the <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_isr.md">EvtInterruptIsr</a> callback function.

For more information about handling interrupts in framework-based drivers, see <a href="https://msdn.microsoft.com/08460510-6e5f-4c02-8086-9caa9b4b4c2d">Handling Hardware Interrupts</a>.

In KMDF 1.11 and later, a driver can call <b>WdfInterruptQueueDpcForIsr</b> from a passive-level ISR.  Note that a driver can register a work item or a DPC but not both.

The following code example shows how an <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_isr.md">EvtInterruptIsr</a> callback function should queue an <a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_dpc.md">EvtInterruptDpc</a> callback function.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** | 1.0 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfinterrupt.h (include Wdf.h) |
| **Library** |  |
| **IRQL** | <=DIRQL |
| **DDI compliance rules** | DriverCreate |

## See Also

<dl>
<dt>
<a href="..\wdfinterrupt\nf-wdfinterrupt-wdfinterruptcreate.md">WdfInterruptCreate</a>
</dt>
<dt>
<a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_dpc.md">EvtInterruptDpc</a>
</dt>
<dt>
<a href="..\wdfinterrupt\nc-wdfinterrupt-evt_wdf_interrupt_isr.md">EvtInterruptIsr</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WdfInterruptQueueDpcForIsr method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>