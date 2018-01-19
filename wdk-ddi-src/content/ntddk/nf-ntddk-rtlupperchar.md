---
UID : NF:ntddk.RtlUpperChar
title : RtlUpperChar function
author : windows-driver-content
description : The RtlUpperChar routine converts the specified character to uppercase.
old-location : kernel\rtlupperchar.htm
old-project : kernel
ms.assetid : a87e9f52-a136-492e-bfb3-dfbbea8b79e0
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlUpperChar
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlUpperChar
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
req.irql : <=APC_LEVEL
req.typenames : WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---


# RtlUpperChar function
The <b>RtlUpperChar</b> routine converts the specified character to uppercase.

## Syntax

````
CHAR RtlUpperChar(
  _In_ CHAR Character
);
````

## Parameters

`Character`

Specifies the character to convert.


## Return Value

<b>RtlUpperChar</b> returns the uppercase version of the specified character or returns the value specified by the caller for <i>Character</i> if the specified character cannot be converted.

## Remarks

<b>RtlUpperChar</b> returns the input <i>Character</i> unconverted if it is the lead byte of a multibyte character or if the uppercase equivalent of <i>Character</i> is a double-byte character. To convert such characters, use <b>RtlUpcaseUnicodeChar</b>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h) |
| **Library** |  |
| **IRQL** | <=APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-rtlupcaseunicodechar.md">RtlUpcaseUnicodeChar</a>
</dt>
<dt>
<a href="..\ntddk\nf-ntddk-rtlupperstring.md">RtlUpperString</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20RtlUpperChar routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>