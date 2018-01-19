---
UID : NF:fltkernel.FltQueryEaFile
title : FltQueryEaFile function
author : windows-driver-content
description : FltQueryEaFile returns information about extended-attribute (EA) values for a file.
old-location : ifsk\fltqueryeafile.htm
old-project : ifsk
ms.assetid : 3981ab65-2d21-4188-88dc-04eb7aff0869
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : FltQueryEaFile
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : fltkernel.h
req.include-header : Fltkernel.h
req.target-type : Universal
req.target-min-winverclnt : Available in Microsoft Windows 2000 Update Rollup 1 for SP4, Windows XP SP3, Windows Server 2003 SP1, and later versions of the Windows operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FltQueryEaFile
req.alt-loc : fltmgr.sys
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : FltMgr.lib
req.dll : Fltmgr.sys
req.irql : PASSIVE_LEVEL
req.typenames : EXpsFontRestriction
---


# FltQueryEaFile function
<b>FltQueryEaFile</b> returns information about extended-attribute (EA) values for a file.

## Syntax

````
NTSTATUS FltQueryEaFile(
  _In_      PFLT_INSTANCE Instance,
  _In_      PFILE_OBJECT  FileObject,
  _Out_     PVOID         ReturnedEaData,
  _In_      ULONG         Length,
  _In_      BOOLEAN       ReturnSingleEntry,
  _In_opt_  PVOID         EaList,
  _In_      ULONG         EaListLength,
  _In_opt_  PULONG        EaIndex,
  _In_      BOOLEAN       RestartScan,
  _Out_opt_ PULONG        LengthReturned
);
````

## Parameters

`Instance`

Opaque instance pointer for the minifilter driver instance that the <i>QueryEa</i> operation is to be sent to. The instance must be attached to the volume where the file resides.

`FileObject`

File object pointer for the file.

`ReturnedEaData`

Pointer to a caller-supplied <a href="..\wdm\ns-wdm-_file_full_ea_information.md">FILE_FULL_EA_INFORMATION</a>-structured input buffer where the extended attribute values are to be returned.

`Length`

Length, in bytes, of the buffer that the <i>ReturnedEaData</i> parameter points to.

`ReturnSingleEntry`

Set to <b>TRUE</b> if <b>FltQueryEaFile</b> should return only the first entry that is found.

`EaList`

Pointer to a caller-supplied <a href="..\ntifs\ns-ntifs-_file_get_ea_information.md">FILE_GET_EA_INFORMATION</a>-structured input buffer specifying the extended attributes to be queried. This parameter is optional and can be <b>NULL</b>.

`EaListLength`

Length, in bytes, of the buffer that the <i>EaList</i> parameter points to.

`EaIndex`

Index of the entry at which to begin scanning the file's extended-attribute list. This parameter is ignored if the <i>EaList</i> parameter points to a nonempty list. This parameter is optional and can be <b>NULL</b>.

`RestartScan`

Set to <b>TRUE</b> if <b>FltQueryEaFile</b> should begin the scan at the first entry in the file's extended-attribute list. If this parameter is not set to <b>TRUE</b>, the scan is resumed from a previous call to <b>FltQueryEaFile</b>.

`LengthReturned`

Pointer to a caller-allocated variable that receives the size, in bytes, of the information returned in the <i>ReturnedEaData</i> buffer. This parameter is optional and can be <b>NULL</b>.


## Return Value

<b>FltQueryEaFile</b> returns STATUS_SUCCESS or an appropriate NTSTATUS value such as the following: 
<dl>
<dt><b>STATUS_EAS_NOT_SUPPORTED</b></dt>
</dl>The file system does not support extended attributes. This is an error code. 
<dl>
<dt><b>STATUS_FLT_DELETING_OBJECT</b></dt>
</dl>The instance or volume is being torn down. This is an error code. 
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl><b>FltQueryEaFile</b> encountered a pool allocation failure. This is an error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fltkernel.h (include Fltkernel.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\ns-wdm-_file_full_ea_information.md">FILE_FULL_EA_INFORMATION</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_file_get_ea_information.md">FILE_GET_EA_INFORMATION</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltseteafile.md">FltSetEaFile</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-iocheckeabuffervalidity.md">IoCheckEaBufferValidity</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FltQueryEaFile function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>