---
UID : NF:storport.StorPortWriteRegisterBufferUlong
title : StorPortWriteRegisterBufferUlong function
author : windows-driver-content
description : The StorPortWriteRegisterBufferUlong routine transfers a given number of ULONG values from a buffer to the HBA.
old-location : storage\storportwriteregisterbufferulong.htm
old-project : storage
ms.assetid : a610f6c5-6627-406e-9b33-f321c6d55a89
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortWriteRegisterBufferUlong
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortWriteRegisterBufferUlong
req.alt-loc : Storport.lib,Storport.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Storport.lib
req.dll : 
req.irql : 
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortWriteRegisterBufferUlong function
The <b>StorPortWriteRegisterBufferUlong</b> routine transfers a given number of ULONG values from a buffer to the HBA.

## Syntax

````
STORPORT_API VOID StorPortWriteRegisterBufferUlong(
  _In_ PVOID  HwDeviceExtension,
  _In_ PULONG Register,
  _In_ PULONG Buffer,
  _In_ ULONG  Count
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension. This is a per HBA storage area that the port driver allocates and initializes on behalf of the miniport driver. Miniport drivers usually store HBA-specific information in this extension, such as the state of the HBA and the mapped access ranges for the HBA. This area is available to the miniport driver immediately after the miniport driver calls <a href="..\storport\nf-storport-storportinitialize.md">StorPortInitialize</a>. The port driver frees this memory when it removes the device.

`Register`

Pointer to the register. The given <i>Register</i> must be in a mapped memory space range that was returned by <a href="..\storport\nf-storport-storportgetdevicebase.md">StorPortGetDeviceBase</a>.

`Buffer`

Pointer to a buffer containing the data to be written.

`Count`

Specifies the number of ULONG values to be transferred to the HBA.


## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\storport\nf-storport-storportwriteregisterbufferulong.md">StorPortWriteRegisterBufferUlong</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortWriteRegisterBufferUlong routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>