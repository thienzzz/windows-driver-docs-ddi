---
UID : NF:storport.StorPortGetMSIInfo
title : StorPortGetMSIInfo function
author : windows-driver-content
description : The StorPortGetMSIInfo routine retrieves the message signaled interrupt (MSI) information for the specified message.
old-location : storage\storportgetmsiinfo.htm
old-project : storage
ms.assetid : 3c98c04c-246a-42a0-bb40-f7771f7ae968
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortGetMSIInfo
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : This routine is available starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortGetMSIInfo
req.alt-loc : storport.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : Any level.
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortGetMSIInfo function
The <b>StorPortGetMSIInfo</b> routine retrieves the message signaled interrupt (MSI) information for the specified message.

## Syntax

````
ULONG StorPortGetMSIInfo(
  _In_  PVOID                          HwDeviceExtension,
  _In_  ULONG                          MessageId,
  _Out_ PMESSAGE_INTERRUPT_INFORMATION InterruptInfo
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension for the host bus adapter (HBA).

`MessageId`

The identifier of the message for which the information is retrieved.

`InterruptInfo`

A pointer to a miniport driver-provided <a href="..\storport\ns-storport-_message_interrupt_information.md">MESSAGE_INTERRUPT_INFORMATION</a> structure that receives the information for the message specified by the <i>MessageId</i> parameter.


## Return Value

<b>StorPortGetMSIInfo</b> returns one of the status codes:
<dl>
<dt><b>STOR_STATUS_NOT_IMPLEMENTED</b></dt>
</dl>This function is not implemented on the active operating system.
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>Indicates that the MSI information was successfully received for the specified message.
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl><i>HwDeviceExtension</i> passed was <b>NULL</b>.

-or-

The pointer in <i>InterruptInfo</i> for the structure to receive the information is <b>NULL</b>.

-or-

<i>MessageId</i> passed to the function is incorrect.
<dl>
<dt><b>STOR_STATUS_INVALID_DEVICE_REQUEST</b></dt>
</dl>The HBA does not support MSI.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** | Any level. |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\storport\ns-storport-_message_interrupt_information.md">MESSAGE_INTERRUPT_INFORMATION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortGetMSIInfo routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>