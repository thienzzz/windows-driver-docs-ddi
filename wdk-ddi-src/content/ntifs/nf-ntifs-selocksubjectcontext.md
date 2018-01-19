---
UID : NF:ntifs.SeLockSubjectContext
title : SeLockSubjectContext function
author : windows-driver-content
description : The SeLockSubjectContext routine locks the primary and impersonation tokens of a captured subject context.
old-location : ifsk\selocksubjectcontext.htm
old-project : ifsk
ms.assetid : 032e203a-9cb0-4232-91fc-883528e15a81
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : SeLockSubjectContext
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
req.alt-api : SeLockSubjectContext
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
req.typenames : TOKEN_TYPE
---


# SeLockSubjectContext function
The <b>SeLockSubjectContext</b> routine locks the primary and impersonation tokens of a captured subject context.

## Syntax

````
VOID SeLockSubjectContext(
  _In_ PSECURITY_SUBJECT_CONTEXT SubjectContext
);
````

## Parameters

`SubjectContext`

Pointer to a SECURITY_SUBJECT_CONTEXT structure returned by a call to <b>SeCaptureSubjectContext</b>.


## Return Value

None

## Remarks

<b>SeLockSubjectContext</b> acquires read locks on the primary and impersonation tokens of a captured subject context.

To capture a subject context, use <b>SeCaptureSubjectContext</b>.

Each call to <b>SeLockSubjectContext</b> must be matched by a subsequent call to <b>SeUnlockSubjectContext</b>.

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
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ntifs\nf-ntifs-secapturesubjectcontext.md">SeCaptureSubjectContext</a>
</dt>
<dt>
<a href="..\wdm\ns-wdm-_security_subject_context.md">SECURITY_SUBJECT_CONTEXT</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-seunlocksubjectcontext.md">SeUnlockSubjectContext</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20SeLockSubjectContext routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>