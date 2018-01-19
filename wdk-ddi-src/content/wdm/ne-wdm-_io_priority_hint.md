---
UID : NE:wdm._IO_PRIORITY_HINT
title : _IO_PRIORITY_HINT
author : windows-driver-content
description : The IO_PRIORITY_HINT enumeration type specifies the priority hint for an IRP.
old-location : kernel\io_priority_hint.htm
old-project : kernel
ms.assetid : 38d19398-b34f-4934-b643-df119ebd9711
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _IO_PRIORITY_HINT, IO_PRIORITY_HINT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IO_PRIORITY_HINT
req.alt-loc : wdm.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : IO_PRIORITY_HINT
req.product : Windows 10 or later.
---

# _IO_PRIORITY_HINT Enumeration
The <b>IO_PRIORITY_HINT</b> enumeration type specifies the <a href="https://msdn.microsoft.com/c34afff2-32f2-451b-ab16-ff048d5c3204">priority hint</a> for an IRP.

## Syntax
````
typedef enum _IO_PRIORITY_HINT { 
  IoPriorityVeryLow   = 0,
  IoPriorityLow       = 1,
  IoPriorityNormal    = 2,
  IoPriorityHigh      = 3,
  IoPriorityCritical  = 4,
  MaxIoPriorityTypes  = 5
} IO_PRIORITY_HINT;
````

## Constants

<table>

<tr>
<td>IoPriorityCritical</td>
<td>Specifies the highest-priority hint level. This value is reserved for use by the system.</td>
</tr>

<tr>
<td>IoPriorityHigh</td>
<td>Specifies a high-priority hint level. This value is reserved for use by the system.</td>
</tr>

<tr>
<td>IoPriorityLow</td>
<td>Specifies a low-priority hint level.</td>
</tr>

<tr>
<td>IoPriorityNormal</td>
<td>Specifies a normal-priority hint level. This value is the default setting for an IRP.</td>
</tr>

<tr>
<td>IoPriorityVeryLow</td>
<td>Specifies the lowest possible priority hint level. The system uses this value for background I/O operations.</td>
</tr>

<tr>
<td>MaxIoPriorityTypes</td>
<td>Marks the limit for priority hints. Any priority hint value must be less than <b>MaxIoPriorityTypes</b>.</td>
</tr>
</table>

## Remarks

For more information about priority hints, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565403">Using IRP Priority Hints</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-iogetiopriorityhint.md">IoGetIoPriorityHint</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iosetiopriorityhint.md">IoSetIoPriorityHint</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IO_PRIORITY_HINT enumeration%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>