---
UID: NC:wdfdmaenabler.EVT_WDF_DMA_ENABLER_ENABLE
title: EVT_WDF_DMA_ENABLER_ENABLE
author: windows-driver-content
description: A driver's EvtDmaEnablerEnable event callback function enables a device's DMA capability after the device enters its working (D0) state.
old-location: wdf\evtdmaenablerenable.htm
old-project: wdf
ms.assetid: b6344a06-98ee-48c0-8fd5-76edfc71af2b
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DFDmaObjectRef_ca81d643-d2a6-4f88-9c6e-80c5681b76d1.xml, EVT_WDF_DMA_ENABLER_ENABLE, EVT_WDF_DMA_ENABLER_ENABLE callback, EvtDmaEnablerEnable, EvtDmaEnablerEnable callback function, kmdf.evtdmaenablerenable, wdf.evtdmaenablerenable, wdfdmaenabler/EvtDmaEnablerEnable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wdfdmaenabler.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
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
req.irql: PASSIVE_LEVEL (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WdfDmaEnabler.h
api_name:
-	EvtDmaEnablerEnable
product:
- Windows
targetos: Windows
req.typenames: 
---

# EVT_WDF_DMA_ENABLER_ENABLE callback function


## -description


<p class="CCE_Message">[Applies to KMDF only]

A driver's <i>EvtDmaEnablerEnable</i> event callback function enables a device's DMA capability after the device enters its working (D0) state. 


## -parameters




### -param DmaEnabler [in]

A handle to a DMA enabler object. 


## -returns



<i>EvtDmaEnablerEnable</i>  must return STATUS_SUCCESS or another status value for which <a href="https://msdn.microsoft.com/fe823930-e3ff-4c95-a640-bb6470c95d1d">NT_SUCCESS</a>(<i>status</i>) equals <b>TRUE</b>, if it encounters no errors. Otherwise, this callback function must return a status value for which NT_SUCCESS(<i>status</i>) equals <b>FALSE</b>. 




## -remarks



To register an <i>EvtDmaEnablerEnable</i> callback function, a function driver for a DMA device places the callback function's address in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551290">WDF_DMA_ENABLER_CONFIG</a> structure before the driver calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff546983">WdfDmaEnablerCreate</a>.

For more information about the <i>EvtDmaEnablerEnable</i> callback function, see <a href="https://msdn.microsoft.com/abbb8f60-560f-41c9-85c5-1ec82078b99e">Supporting Power Management for DMA Devices</a>.

The <i>EvtDmaEnablerEnable</i> callback function is called at IRQL = PASSIVE_LEVEL. You should not make this callback function <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/creating-pageable-code-in-a-kmdf-driver">pageable</a>.


#### Examples

To define an <i>EvtDmaEnablerEnable</i> callback function, you must first provide a function declaration that identifies the type of callback function you’re defining. Windows provides a set of callback function types for drivers. Declaring a function using the callback function types helps <a href="https://msdn.microsoft.com/2F3549EF-B50F-455A-BDC7-1F67782B8DCA">Code Analysis for Drivers</a>, <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it’s a requirement for writing drivers for the Windows operating system.

For example, to define an <i>EvtDmaEnablerEnable</i> callback function that is named <i>MyDmaEnablerEnable</i>, use the <b>EVT_WDF_DMA_ENABLER_ENABLE</b> type as shown in this code example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>EVT_WDF_DMA_ENABLER_ENABLE  MyDmaEnablerEnable;</pre>
</td>
</tr>
</table></span></div>
Then, implement your callback function as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>_Use_decl_annotations_
NTSTATUS
 MyDmaEnablerEnable (
    WDFDMAENABLER  DmaEnabler
    )
  {...}</pre>
</td>
</tr>
</table></span></div>
The <b>EVT_WDF_DMA_ENABLER_ENABLE</b> function type is defined in the WdfDmaEnabler.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition. The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the <b>EVT_WDF_DMA_ENABLER_ENABLE</b> function type in the header file are used. For more information about the requirements for function declarations, see <a href="https://msdn.microsoft.com/73a408ba-0219-4fde-8dad-ca330e4e67c3">Declaring Functions by Using Function Role Types for KMDF Drivers</a>. For information about _Use_decl_annotations_, see <a href="https://msdn.microsoft.com/en-US/library/c0aa268d-6fa3-4ced-a8c6-f7652b152e61">Annotating Function Behavior</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a39e19b-9720-4641-83f0-654a5f116432">EvtDmaEnablerDisable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551290">WDF_DMA_ENABLER_CONFIG</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546983">WdfDmaEnablerCreate</a>
 

 

