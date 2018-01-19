---
UID : NF:fltkernel.FltFreeFileLock
title : FltFreeFileLock function
author : windows-driver-content
description : The FltFreeFileLock routine uninitializes and frees an initialized FILE_LOCK structure.
old-location : ifsk\fltfreefilelock.htm
old-project : ifsk
ms.assetid : bcf2ac97-0aa2-4464-a045-b98866351243
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : FltFreeFileLock
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : fltkernel.h
req.include-header : Fltkernel.h
req.target-type : Universal
req.target-min-winverclnt : This routine is available on Microsoft Windows XP SP2, Microsoft Windows Server 2003 SP1, and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FltFreeFileLock
req.alt-loc : FltMgr.lib,FltMgr.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : FltMgr.lib
req.dll : 
req.irql : <= APC_LEVEL
req.typenames : EXpsFontRestriction
---


# FltFreeFileLock function
The <b>FltFreeFileLock</b> routine uninitializes and frees an initialized FILE_LOCK structure.

## Syntax

````
VOID FltFreeFileLock(
  _In_ PFILE_LOCK FileLock
);
````

## Parameters

`FileLock`

Pointer to the FILE_LOCK structure. This structure must have been initialized by a previous call to <a href="..\fltkernel\nf-fltkernel-fltallocatefilelock.md">FltAllocateFileLock</a> or <a href="..\fltkernel\nf-fltkernel-fltinitializefilelock.md">FltInitializeFileLock</a>.


## Return Value

None

## Remarks

The FILE_LOCK structure is opaque: that is, its members are reserved for system use. 

To allocate and initialize a new file lock structure, call <a href="..\fltkernel\nf-fltkernel-fltallocatefilelock.md">FltAllocateFileLock</a>. 

It is a programming error to call <b>FltFreeFileLock</b> for a FILE_LOCK structure that has already been uninitialized by a call to <a href="..\fltkernel\nf-fltkernel-fltuninitializefilelock.md">FltUninitializeFileLock</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fltkernel.h (include Fltkernel.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltallocatefilelock.md">FltAllocateFileLock</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltchecklockforreadaccess.md">FltCheckLockForReadAccess</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltchecklockforwriteaccess.md">FltCheckLockForWriteAccess</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltinitializefilelock.md">FltInitializeFileLock</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltprocessfilelock.md">FltProcessFileLock</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltuninitializefilelock.md">FltUninitializeFileLock</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlfreefilelock.md">FsRtlFreeFileLock</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FltFreeFileLock routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>