---
UID : NF:wdm.RtlxUnicodeStringToAnsiSize
title : RtlxUnicodeStringToAnsiSize function
author : windows-driver-content
description : The RtlxUnicodeStringToAnsiSize routine returns the number of bytes required for a null-terminated ANSI string that is equivalent to a specified Unicode string.
old-location : kernel\rtlxunicodestringtoansisize.htm
old-project : kernel
ms.assetid : dff228e5-14ea-4ec0-a7f1-247137f9e70d
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlxUnicodeStringToAnsiSize
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlxUnicodeStringToAnsiSize
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : PASSIVE_LEVEL
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# RtlxUnicodeStringToAnsiSize function
The <b>RtlxUnicodeStringToAnsiSize</b> routine returns the number of bytes required for a null-terminated ANSI string that is equivalent to a specified Unicode string.

## Syntax

````
ULONG RtlxUnicodeStringToAnsiSize(
  _In_ PCUNICODE_STRING UnicodeString
);
````

## Parameters

`UnicodeString`

Pointer to the Unicode string for which to compute the number of bytes required for an equivalent null-terminated ANSI string.


## Return Value

If the Unicode string can be translated into an ANSI string using the current system locale information, <b>RtlxUnicodeStringToAnsiSize</b> returns the number of bytes required for an equivalent null-terminated ANSI string. Otherwise, it returns zero.

## Remarks

The Unicode string is interpreted for the current system locale.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-rtlunicodestringtoansisize.md">RtlUnicodeStringToAnsiSize</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20RtlxUnicodeStringToAnsiSize routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>