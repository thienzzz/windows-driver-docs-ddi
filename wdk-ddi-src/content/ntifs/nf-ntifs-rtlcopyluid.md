---
UID : NF:ntifs.RtlCopyLuid
title : RtlCopyLuid function
author : windows-driver-content
description : The RtlCopyLuid routine copies a locally unique identifier (LUID) to a buffer.
old-location : ifsk\rtlcopyluid.htm
old-project : ifsk
ms.assetid : ebda25f4-77d6-4178-9ff8-b1f0e95df9f0
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RtlCopyLuid
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlCopyLuid
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
req.irql : < DISPATCH_LEVEL
req.typenames : TOKEN_TYPE
---


# RtlCopyLuid function
The <b>RtlCopyLuid</b> routine copies a locally unique identifier (LUID) to a buffer.

## Syntax

````
VOID RtlCopyLuid(
  _Out_ PLUID DestinationLuid,
  _In_  PLUID SourceLuid
);
````

## Parameters

`DestinationLuid`

Pointer to a caller-allocated buffer to receive a copy of the source LUID structure. The buffer must be at least <b>sizeof(</b>LUID<b>)</b>.

`SourceLuid`

Pointer to the source LUID structure to be copied.


## Return Value

None

## Remarks

<b>RtlCopyLuid</b> does not check whether the LUID at <i>SourceLuid</i> is structurally valid. 

For more information about security and access control, see the documentation on these topics in the Microsoft Windows SDK.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h) |
| **Library** |  |
| **IRQL** | < DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff561842">RtlEqualLuid</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-sequeryauthenticationidtoken.md">SeQueryAuthenticationIdToken</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RtlCopyLuid routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>