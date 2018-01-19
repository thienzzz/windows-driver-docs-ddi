---
UID : NF:ntifs.IoInitializePriorityInfo
title : IoInitializePriorityInfo function
author : windows-driver-content
description : The IoInitializePriorityInfo routine initializes a structure of type IO_PRIORITY_INFO.
old-location : ifsk\ioinitializepriorityinfo.htm
old-project : ifsk
ms.assetid : 21aa5850-1984-4ab8-8e7c-3028fc87680b
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : IoInitializePriorityInfo
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h, Fltkernel.h
req.target-type : Desktop
req.target-min-winverclnt : This routine is available starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoInitializePriorityInfo
req.alt-loc : ntifs.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : TOKEN_TYPE
---


# IoInitializePriorityInfo function
The <b>IoInitializePriorityInfo</b> routine initializes a structure of type <a href="..\ntifs\ns-ntifs-_io_priority_info.md">IO_PRIORITY_INFO</a>.

## Syntax

````
VOID IoInitializePriorityInfo(
  _In_ PIO_PRIORITY_INFO PriorityInfo
);
````

## Parameters

`PriorityInfo`

Pointer to a structure, of type IO_PRIORITY_INFO, to be initialized. This parameter is required and cannot be <b>NULL</b>.


## Return Value

None.

## Remarks

The <b>IoInitializePriorityInfo</b> routine is used to initialize the IO_PRIORITY_INFO structure that is utilized by the <a href="..\fltkernel\nf-fltkernel-fltretrieveiopriorityinfo.md">FltRetrieveIoPriorityInfo</a> routine.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h, Fltkernel.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltapplypriorityinfothread.md">FltApplyPriorityInfoThread</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltretrieveiopriorityinfo.md">FltRetrieveIoPriorityInfo</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_io_priority_info.md">IO_PRIORITY_INFO</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20IoInitializePriorityInfo routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>