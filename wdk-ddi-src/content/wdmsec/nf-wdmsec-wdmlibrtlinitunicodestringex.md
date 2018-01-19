---
UID : NF:wdmsec.WdmlibRtlInitUnicodeStringEx
title : WdmlibRtlInitUnicodeStringEx function
author : windows-driver-content
description : The WdmlibRtlInitUnicodeStringEx function initializes a counted string of Unicode characters.
old-location : kernel\wdmlibrtlinitunicodestringex.htm
old-project : kernel
ms.assetid : 79DEDC5B-2A9B-4493-9CB3-7290BEBBD291
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : WdmlibRtlInitUnicodeStringEx
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdmsec.h
req.include-header : Wdmsec.h, Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WdmlibRtlInitUnicodeStringEx,RtlInitUnicodeString
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
req.irql : See Remarks section.
req.typenames : WORK_QUEUE_ITEM, *PWORK_QUEUE_ITEM
req.product : Windows 10 or later.
---


# WdmlibRtlInitUnicodeStringEx function
The <b>WdmlibRtlInitUnicodeStringEx</b> function initializes a counted string of Unicode characters.

## Syntax

````
NTSTATUS WdmlibRtlInitUnicodeStringEx(
  _Out_    PUNICODE_STRING DestinationString,
  _In_opt_ PCWSTR          SourceString
);
````

## Parameters

`DestinationString`

A pointer to the <a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structure to be initialized.

`SourceString`

A pointer to a null-terminated wide-character string. This string is used to initialize the counted string pointed to by <i>DestinationString</i>.


## Return Value

None

## Remarks

The routine copies the <i>SourceString</i> pointer value to the <b>Buffer</b> member of the <a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structure pointed to by <i>DestinationString</i>. The <b>Length</b> member of this structure is set to the length, in bytes, of the source string, excluding the terminating null. The <b>MaximumLength</b> member of the structure is set to the length, in bytes, of the source string, including the terminating null. If <i>SourceString</i> is <b>NULL</b>, <b>Length</b> and <b>MaximumLength</b> are both set to zero.

<b>WdmlibRtlInitUnicodeStringEx</b> does not alter the source string pointed to by <i>SourceString</i>.

Callers of <b>WdmlibRtlInitUnicodeStringEx</b> can be running at IRQL &lt;= DISPATCH_LEVEL if the <i>DestinationString</i> buffer is nonpageable. Usually, callers run at IRQL = PASSIVE_LEVEL because most other <b>Rtl<i>Xxx</i>String</b> routines cannot be called at IRQL &gt; PASSIVE_LEVEL.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdmsec.h (include Wdmsec.h, Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | See Remarks section. |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ntstrsafe\nf-ntstrsafe-rtlunicodestringinit.md">RtlUnicodeStringInit</a>
</dt>
<dt>
<a href="..\ntstrsafe\nf-ntstrsafe-rtlunicodestringinitex.md">RtlUnicodeStringInitEx</a>
</dt>
<dt>
<a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20WdmlibRtlInitUnicodeStringEx function%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>