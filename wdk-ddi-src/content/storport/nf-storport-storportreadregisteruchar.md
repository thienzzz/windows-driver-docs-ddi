---
UID : NF:storport.StorPortReadRegisterUchar
title : StorPortReadRegisterUchar function
author : windows-driver-content
description : The StorPortReadRegisterUchar routine reads a value from a specified register address.
old-location : storage\storportreadregisteruchar.htm
old-project : storage
ms.assetid : 1edf800d-f097-4d3f-ae89-1b11e4f82f2d
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortReadRegisterUchar
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
req.alt-api : StorPortReadRegisterUchar
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


# StorPortReadRegisterUchar function
The <b>StorPortReadRegisterUchar</b> routine reads a value from a specified register address.

## Syntax

````
STORPORT_API UCHAR StorPortReadRegisterUchar(
  _In_ PVOID  HwDeviceExtension,
  _In_ PUCHAR Register
);
````

## Parameters

`HwDeviceExtension`

Pointer to the hardware device extension.

`Register`

Pointer to the register where the data is to be read.


## Return Value

<b>StorPortReadRegisterUchar</b> returns an unsigned character of data read from the indicated register address.

## Remarks

For more information, see <a href="..\srb\nf-srb-scsiportreadregisteruchar.md">ScsiPortReadRegisterUchar</a>. For a buffered version of this routine, see <a href="..\storport\nf-storport-storportreadregisterbufferuchar.md">StorPortReadRegisterBufferUchar</a>.

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
<a href="..\srb\nf-srb-scsiportreadregisteruchar.md">ScsiPortReadRegisterUchar</a>
</dt>
<dt>
<a href="..\storport\nf-storport-storportreadregisterbufferuchar.md">StorPortReadRegisterBufferUchar</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortReadRegisterUchar routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>