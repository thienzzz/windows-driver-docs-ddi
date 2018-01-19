---
UID : NF:wdfinterrupt.WDF_INTERRUPT_EXTENDED_POLICY_INIT
title : WDF_INTERRUPT_EXTENDED_POLICY_INIT function
author : windows-driver-content
description : The WDF_INTERRUPT_EXTENDED_POLICY_INIT function initializes a WDF_INTERRUPT_EXTENDED_POLICY structure.
old-location : wdf\wdf_interrupt_extended_policy_init.htm
old-project : wdf
ms.assetid : fcc1e631-c77b-483b-9b5e-ec8d643f9930
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WDF_INTERRUPT_EXTENDED_POLICY_INIT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfinterrupt.h
req.include-header : Wdf.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.9
req.umdf-ver : 2.0
req.alt-api : WDF_INTERRUPT_EXTENDED_POLICY_INIT
req.alt-loc : wdfinterrupt.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : Any level
req.typenames : WDF_INTERRUPT_PRIORITY, *PWDF_INTERRUPT_PRIORITY
req.product : Windows 10 or later.
---


# WDF_INTERRUPT_EXTENDED_POLICY_INIT function
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_INTERRUPT_EXTENDED_POLICY_INIT</b> function initializes a <a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_extended_policy.md">WDF_INTERRUPT_EXTENDED_POLICY</a> structure.

## Syntax

````
VOID WDF_INTERRUPT_EXTENDED_POLICY_INIT(
  _Out_ PWDF_INTERRUPT_EXTENDED_POLICY PolicyAndGroup
);
````

## Parameters

`ExtendedPolicy`




## Return Value

None.

## Remarks

The <b>WDF_INTERRUPT_EXTENDED_POLICY_INIT</b> function zeros the specified <a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_extended_policy.md">WDF_INTERRUPT_EXTENDED_POLICY</a> structure and sets the structure's <b>Size</b> member. It also sets the structure's <b>Policy</b> member to <b>WdfIrqPolicyMachineDefault</b> and sets the structure's <b>Priority</b> member to <b>WdfIrqPriorityUndefined</b>.

For a code example that uses <b>WDF_INTERRUPT_EXTENDED_POLICY_INIT</b>, see <a href="..\wdfinterrupt\nf-wdfinterrupt-wdfinterruptsetextendedpolicy.md">WdfInterruptSetExtendedPolicy</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** | 1.9 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfinterrupt.h (include Wdf.h) |
| **Library** |  |
| **IRQL** | Any level |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wudfinterrupt\ns-wudfinterrupt-_wdf_interrupt_extended_policy.md">WDF_INTERRUPT_EXTENDED_POLICY</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20WDF_INTERRUPT_EXTENDED_POLICY_INIT function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>