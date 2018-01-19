---
UID : NF:bdasup.BdaCheckChanges
title : BdaCheckChanges function
author : windows-driver-content
description : The BdaCheckChanges function verifies a new set of BDA topology changes before they are committed.
old-location : stream\bdacheckchanges.htm
old-project : stream
ms.assetid : 4831e13b-19e7-458c-a392-a135d43fc989
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : BdaCheckChanges
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : bdasup.h
req.include-header : Bdasup.h
req.target-type : Desktop
req.target-min-winverclnt : Available on Microsoft Windows XP and later operating systems. BdaCheckChanges is available on the Windows 2000 platform only if Microsoft DirectX 9.0 and later is installed on that platform.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : BdaCheckChanges
req.alt-loc : Bdasup.lib,Bdasup.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Bdasup.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : KSP_BDA_NODE_PIN, *PKSP_BDA_NODE_PIN
---


# BdaCheckChanges function
The <b>BdaCheckChanges</b> function verifies a new set of BDA topology changes before they are committed.

## Syntax

````
NTSTATUS BdaCheckChanges(
  _In_ PIRP Irp
);
````

## Parameters

`pIrp`




## Return Value

Returns STATUS_SUCCESS or an appropriate error code. Returns the result that the <b>BdaCommitChanges</b> function would have returned.

## Remarks

A BDA minidriver calls the <b>BdaCheckChanges</b> function to verify a group of BDA topology changes after the minidriver receives a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563407">KSMETHOD_BDA_CHECK_CHANGES</a> request of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563403">KSMETHODSETID_BdaChangeSync</a> method set from the network provider. BDA minidrivers define dispatch and filter-automation tables so that those minidrivers either dispatch the <b>BdaCheckChanges</b> function directly or intercept this request using an internal method (<a href="..\ks\nc-ks-pfnkshandler.md">KStrMethodHandler</a>), which then calls the <b>BdaCheckChanges</b> function. For example, BDA minidrivers that intercept this request can obtain a pointer to the BDA filter from the passed IRP so that they can validate the new list of resources for the filter. See <a href="https://msdn.microsoft.com/1c0dace6-b618-4705-bf5d-65457d14c072">Defining Automation Tables</a> and <a href="https://msdn.microsoft.com/1833864a-5759-437c-ba60-0b38602d9e41">Changing BDA Filter Properties</a> for more information.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | bdasup.h (include Bdasup.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\bdasup\nf-bdasup-bdacommitchanges.md">BdaCommitChanges</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563407">KSMETHOD_BDA_CHECK_CHANGES</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563403">KSMETHODSETID_BdaChangeSync</a>
</dt>
<dt>
<a href="..\ks\nc-ks-pfnkshandler.md">KStrMethodHandler</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20BdaCheckChanges function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>