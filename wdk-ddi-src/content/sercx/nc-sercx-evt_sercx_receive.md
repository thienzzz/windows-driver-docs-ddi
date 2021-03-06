---
UID: NC:sercx.EVT_SERCX_RECEIVE
title: EVT_SERCX_RECEIVE
author: windows-driver-content
description: The EvtSerCxReceive event callback function prepares the serial controller device (UART) to do a read (receive) operation.
old-location: serports\evtsercxreceive.htm
old-project: serports
ms.assetid: C862D632-5425-4EEB-9C5D-BC3721D9F132
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 1/EvtSerCxReceive, EVT_SERCX_RECEIVE, EVT_SERCX_RECEIVE callback, EvtSerCxReceive, EvtSerCxReceive callback function [Serial Ports], serports.evtsercxreceive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: sercx.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows 8.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: Called at IRQL <= DISPATCH_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	1.0\Sercx.h
api_name:
-	EvtSerCxReceive
product:
- Windows
targetos: Windows
req.typenames: 
---

# EVT_SERCX_RECEIVE callback function


## -description


The <i>EvtSerCxReceive</i> event callback function prepares the serial controller device (UART) to do a read (receive) operation.


## -parameters




### -param Device [in]

A WDFDEVICE handle to the framework device object that represents the serial controller.


### -param Length [in]

The number of bytes to be received. The controller driver can use this value as a hint to decide whether to use PIO or DMA to perform the data transfer.


## -returns



The <i>EvtSerCxReceive</i> function returns STATUS_SUCCESS if the call is successful. Otherwise, it returns an appropriate error status code.




## -remarks



The serial framework extension (SerCx) calls this function to configure the controller hardware to receive data. If necessary, the <i>EvtSerCxReceive</i> function can enable interrupts.

The <i>EvtSerCxReceive</i> function does not necessarily read the input data from the receive FIFO buffer. Depending on the serial controller hardware or the type of transfer, this function might set up a DMA operation to read the data, or it might schedule a transmit/receive DPC function to read the data. The serial controller driver implements this DPC function to receive data from the controller and to transmit data to the serial controller. During the DPC, the DPC function determines whether data is available to be received and, if so, uses PIO to read the data from the receive FIFO in the serial controller.

If the receive FIFO in the serial controller is empty or nearly empty, but the FIFO's high-water-mark interrupt is enabled, the DPC routine can simply return. Later, the controller driver's ISR can schedule the DPC routine to run, and this routine can read more data from the receive FIFO.

To register an <i>EvtSerCxReceive</i> callback function, the controller driver calls the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406711">SerCxInitialize</a> method during the <a href="https://msdn.microsoft.com/b20db029-ee2c-4fb1-bd69-ccd2e37fdc9a">EvtDriverDeviceAdd</a> callback.


#### Examples

The function type for this callback is declared in Sercx.h, as follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef NTSTATUS
  EVT_SERCX_RECEIVE(
    __in WDFDEVICE Device
    );</pre>
</td>
</tr>
</table></span></div>
To define an <i>EvtSerCxReceive</i> callback function that is named <code>MyEvtSerCxReceive</code>, you must first provide a function declaration that <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV) and other verification tools require, as follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>EVT_SERCX_RECEIVE MyEvtSerCxReceive;</pre>
</td>
</tr>
</table></span></div>
Then, implement your callback function as follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>NTSTATUS
  MyEvtSerCxReceive(
    __in WDFDEVICE Device
    )
{ ... }</pre>
</td>
</tr>
</table></span></div>
For more information about SDV requirements for function declarations, see <a href="https://msdn.microsoft.com/73a408ba-0219-4fde-8dad-ca330e4e67c3">Declaring Functions Using Function Role Types for KMDF Drivers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b20db029-ee2c-4fb1-bd69-ccd2e37fdc9a">EvtDriverDeviceAdd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406711">SerCxInitialize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547148">WdfDpcEnqueue</a>
 

 

