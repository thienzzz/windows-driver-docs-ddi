---
UID : NF:ntddk.RtlUpperString
title : RtlUpperString function
author : windows-driver-content
description : The RtlUpperString routine copies the given SourceString to the DestinationString buffer, converting it to uppercase.
old-location : kernel\rtlupperstring.htm
old-project : kernel
ms.assetid : 3a120831-deac-4075-9aa7-8ae39ac29363
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : RtlUpperString
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
req.alt-api : RtlUpperString
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


# RtlUpperString function
The <b>RtlUpperString</b> routine copies the given <i>SourceString</i> to the <i>DestinationString</i> buffer, converting it to uppercase.

## Syntax

````
VOID RtlUpperString(
  _Inout_       PSTRING DestinationString,
  _In_    const STRING  *SourceString
);
````

## Parameters

`DestinationString`

Pointer to the buffer for the converted destination string.

`SourceString`

Pointer to the source string to be converted to uppercase.


## Return Value

None

## Remarks

The <b>MaximumLength</b> and <b>Buffer</b> members of <i>DestinationString</i> are not modified by this routine.

The number of bytes copied from <i>SourceString</i> is either the <b>Length</b> of <i>SourceString</i> or the <b>MaximumLength</b> of <i>DestinationString</i>, whichever is smaller.

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
<a href="..\ntddk\nf-ntddk-rtlupperchar.md">RtlUpperChar</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20RtlUpperString routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>