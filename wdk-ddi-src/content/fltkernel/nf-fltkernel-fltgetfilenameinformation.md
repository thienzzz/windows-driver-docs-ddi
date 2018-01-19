---
UID : NF:fltkernel.FltGetFileNameInformation
title : FltGetFileNameInformation function
author : windows-driver-content
description : The FltGetFileNameInformation routine returns name information for a file or directory.
old-location : ifsk\fltgetfilenameinformation.htm
old-project : ifsk
ms.assetid : 707e7e83-31d8-46cf-a2ef-e53a20edaeff
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : FltGetFileNameInformation
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : fltkernel.h
req.include-header : Fltkernel.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FltGetFileNameInformation
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
req.irql : <= APC_LEVEL
req.typenames : EXpsFontRestriction
---


# FltGetFileNameInformation function
The <b>FltGetFileNameInformation</b> routine returns name information for a file or directory.

## Syntax

````
NTSTATUS FltGetFileNameInformation(
  _In_  PFLT_CALLBACK_DATA         CallbackData,
  _In_  FLT_FILE_NAME_OPTIONS      NameOptions,
  _Out_ PFLT_FILE_NAME_INFORMATION *FileNameInformation
);
````

## Parameters

`CallbackData`

A pointer to the callback data structure for the I/O operation (<a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a>). This parameter is required and cannot be <b>NULL</b>.

`NameOptions`

<a href="https://msdn.microsoft.com/library/windows/hardware/ff544636">FLT_FILE_NAME_OPTIONS</a> value containing flags that specify the format of the name information to be returned, as well as the query method that the Filter Manager is to use. (Additional flags can be used by name provider minifilter drivers to specify name query options. For more information, see <b>FLT_FILE_NAME_OPTIONS</b>.) This parameter is required and cannot be <b>NULL</b>. 

Following are the name format flag values. Only one of the following flags can be specified. (For an explanation of these formats, see <a href="..\fltkernel\ns-fltkernel-_flt_file_name_information.md">FLT_FILE_NAME_INFORMATION</a>.) 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FLT_FILE_NAME_NORMALIZED

</td>
<td>
The <i>FileNameInformation</i> parameter receives the address of a structure containing the normalized name for the file. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_OPENED

</td>
<td>
The <i>FileNameInformation</i> parameter receives the address of a structure containing the name that was used when the file was opened. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_SHORT

</td>
<td>
The <i>FileNameInformation</i> parameter receives the address of a structure containing the short (8.3) name for the file. The short name consists of up to 8 characters, followed immediately by a period and up to 3 more characters. The short name for a file does not include the volume name, directory path, or stream name. 

Not valid in the pre-create path. 

</td>
</tr>
</table>
 

Following are the query method flag values. Only one of the following flags can be specified. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FLT_FILE_NAME_QUERY_DEFAULT

</td>
<td>
If it is not currently safe to query the file system for the file name, <b>FltGetFileNameInformation</b> does nothing. Otherwise, <b>FltGetFileNameInformation</b> queries the Filter Manager's name cache for the file name information. If the name is not found in the cache, <b>FltGetFileNameInformation</b> queries the file system and caches the result. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_QUERY_CACHE_ONLY

</td>
<td>
FltGetFileNameInformation queries the Filter Manager's name cache for the file name information. <b>FltGetFileNameInformation</b> does not query the file system. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_QUERY_FILESYSTEM_ONLY

</td>
<td>
<b>FltGetFileNameInformation</b> queries the file system for the file name information. <b>FltGetFileNameInformation</b> does not query the Filter Manager's name cache, and does not cache the result of the file system query. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_QUERY_ALWAYS_ALLOW_CACHE_LOOKUP

</td>
<td>
<b>FltGetFileNameInformation</b> queries the Filter Manager's name cache for the file name information. If the name is not found in the cache, and it is currently safe to do so, <b>FltGetFileNameInformation</b> queries the file system for the file name information and caches the result. 

</td>
</tr>
</table>
 

Name provider minifilters use the following flags to specify the properties of file name operations. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FLT_FILE_NAME_REQUEST_FROM_CURRENT_PROVIDER

</td>
<td>
A name provider minifilter can use this flag to specify that a name query request should be redirected to itself (the name provider minifilter) rather than being satisfied by the name providers lower in the stack. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_DO_NOT_CACHE

</td>
<td>
This flag denotes that the name retrieved from this query should not be cached. Name provider minifilters use this flag as they perform intermediate queries to generate a name. 

</td>
</tr>
<tr>
<td>
FLT_FILE_NAME_ALLOW_QUERY_ON_REPARSE

</td>
<td>
A name provider minifilter can use this flag to specify that it is safe to query the name in the post-create path even if STATUS_REPARSE was returned. It is the caller's responsibility to ensure that the <b>FileObject-&gt;FileName</b> field was not changed. Do not use this flag with mount points or symbolic link reparse points. 

This flag is available on Microsoft Windows Server 2003 SP1 and later. This flag is also available on Windows 2000 SP4 with Update Rollup 1 and later.

</td>
</tr>
</table>

`FileNameInformation`

A pointer to a caller-allocated variable that receives the address of a system-allocated <a href="..\fltkernel\ns-fltkernel-_flt_file_name_information.md">FLT_FILE_NAME_INFORMATION</a> structure containing the file name information. <b>FltGetFileNameInformation</b> allocates this structure from paged pool. This parameter is required and cannot be <b>NULL</b>.


## Return Value

If the name information is successfully returned, <b>FltGetFileNameInformation</b> returns STATUS_SUCCESS. Otherwise, it returns an appropriate NTSTATUS value such as one of the following: 
<dl>
<dt><b>STATUS_FLT_INVALID_NAME_REQUEST</b></dt>
</dl>One of the following: 

<b>FltGetFileNameInformation</b> cannot get file name information if the <b>TopLevelIrp</b> field of the current thread is not <b>NULL</b>, because the resulting file system recursion could cause deadlocks or stack overflows. (For more information about this issue, see <a href="..\ntifs\nf-ntifs-iogettoplevelirp.md">IoGetTopLevelIrp</a>.) 

<b>FltGetFileNameInformation</b> cannot get file name information in the paging I/O path. 

<b>FltGetFileNameInformation</b> cannot get file name information in the post-close path. 

<b>FltGetFileNameInformation</b> cannot get the short name of a file in the pre-create path. 

STATUS_FLT_INVALID_NAME_REQUEST is an error code.
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl><b>FltGetFileNameInformation</b> encountered a pool allocation failure. This is an error code. 
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>One of the following: 

The <b>FileNameInformation</b> parameter cannot be <b>NULL</b>.

The <i>CallbackData</i> parameter cannot be <b>NULL</b>.

STATUS_INVALID_PARAMETER is an error code.
<dl>
<dt><b>STATUS_FLT_NAME_CACHE_MISS</b></dt>
</dl>The file name information is not found in the name cache and <i>NameOptions</i> includes FLT_FILE_NAME_QUERY_CACHE_ONLY.

-or-

The file name information is not found in the name cache when <i>NameOptions</i> includes FLT_FILE_NAME_QUERY_ALWAYS_ALLOW_CACHE_LOOKUP and the file name information cannot be queried from the file system.

An additional call to <b>FltGetFileNameInformation</b>  with FLT_FILE_NAME_QUERY_FILESYSTEM_ONLY set in <i>NameOptions</i> may return the file name information.
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>If the user opened the file by file ID but does not have traverse privileges for the entire path, <b>FltGetFileNameInformation</b> fails with this return value. 

STATUS_ACCESS_DENIED is an error code. 

-or-

The file is a system file with all access denied.

## Remarks

<b>FltGetFileNameInformation</b> returns the requested name information for the file or directory that is represented by the file object that is the target of the I/O operation. 

For a pre-create operation, if the <b>CallbackData</b> -&gt;<b>Iopb</b> -&gt;<b>OperationFlags</b> member contains the SL_OPEN_TARGET_DIRECTORY bitwise flag, <b>FltGetFileNameInformation</b> returns the name of the containing (parent) directory for the given file. This name is the actual path that the create operation opens.

To parse the contents of the FLT_FILE_NAME_INFORMATION structure returned by <b>FltGetFileNameInformation</b>, call <a href="..\fltkernel\nf-fltkernel-fltparsefilenameinformation.md">FltParseFileNameInformation</a>. (For more information about file name formats, see <a href="..\fltkernel\ns-fltkernel-_flt_file_name_information.md">FLT_FILE_NAME_INFORMATION</a>.) 

After a successful call to <b>FltGetFileNameInformation</b>, the caller is responsible for releasing the pointer returned in the <i>FileNameInformation</i> parameter when the pointer is no longer needed. The caller does this by calling <a href="..\fltkernel\nf-fltkernel-fltreleasefilenameinformation.md">FltReleaseFileNameInformation</a>. 

The caller must not modify the contents of the structure returned in the <i>FileNameInformation</i> parameter because this structure is cached by the Filter Manager so that all minifilter drivers can use it. 

If <b>FltGetFileNameInformation</b> is called in the preoperation callback routine for a create operation to retrieve the opened name, <b>FltGetFileNameInformation</b> succeeds even if the path to the file being opened does not exist on the volume. If <b>FltGetFileNameInformation</b> is called in the preoperation callback routine for a create operation to retrieve the normalized name, <b>FltGetFileNameInformation</b> succeeds even if the final component of the path to the file being opened does not exist on the volume.

In create, hard-link, and rename operations, file name tunneling can cause the final component in normalized file name information that a minifilter driver retrieves in a preoperation callback routine to be invalidated. If a minifilter driver retrieves normalized file name information in a preoperation callback (<a href="..\fltkernel\nc-fltkernel-pflt_pre_operation_callback.md">PFLT_PRE_OPERATION_CALLBACK</a>) routine by calling a routine such as <b>FltGetFileNameInformation</b>, it must call <a href="..\fltkernel\nf-fltkernel-fltgettunneledname.md">FltGetTunneledName</a> from its postoperation callback (<a href="..\fltkernel\nc-fltkernel-pflt_post_operation_callback.md">PFLT_POST_OPERATION_CALLBACK</a>) routine to retrieve the correct file name information for the file. 

For Windows 8.1 and earlier, <b>FltGetFileNameInformation</b> can include a <a href="https://msdn.microsoft.com/41dda6f1-a6d1-4e76-94f3-a72f9e491bee">stream type</a> <i>only</i> when called from a filter’s pre-create callback.  To distinguish between a file’s default stream and metadata streams, this call should be made in the pre-create operation. The resulting stream type will remain valid across the lifetime of the file.

 Prior to Windows 8, Filter Manager obtained the normalized name for a file or directory by collecting the name information for each component of  the file path. This required multiple queries to the file system to compile the complete path. Starting with Windows 8, local file systems support the  <b>FileNormalizedNameInformation</b> file information class and only a single query is necessary to obtain the normalized name. Remote file systems may not support the <b>FileNormalizedNameInformation</b> file information class. When this is the case, a query for each component of the file path is still required to assemble the normalized name. Under certain network conditions, a full name query can require a significant amount of time to complete.

For more information about normalized file name information, see <a href="..\fltkernel\ns-fltkernel-_flt_file_name_information.md">FLT_FILE_NAME_INFORMATION</a>. 

The following paired operations can cause the file name <i>name</i> to be tunneled: 

delete(<i>name</i>)/create(<i>name</i>)

delete(<i>name</i>)/rename(<i>source</i>, <i>name</i>)

rename(<i>name</i>, <i>newname</i>)/create(<i>name</i>)

rename(<i>name</i>, <i>newname</i>)/rename(<i>source</i>, <i>name</i>)

For more information about file name tunneling, see <a href="http://go.microsoft.com/fwlink/p/?linkid=3100&amp;amp;id=172190">Microsoft Knowledge Base Article 172190</a>.

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
<a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a>
</dt>
<dt>
<a href="..\fltkernel\ns-fltkernel-_flt_file_name_information.md">FLT_FILE_NAME_INFORMATION</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544636">FLT_FILE_NAME_OPTIONS</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltgetdestinationfilenameinformation.md">FltGetDestinationFileNameInformation</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltgetfilenameinformationunsafe.md">FltGetFileNameInformationUnsafe</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltgettunneledname.md">FltGetTunneledName</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltparsefilenameinformation.md">FltParseFileNameInformation</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltreferencefilenameinformation.md">FltReferenceFileNameInformation</a>
</dt>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltreleasefilenameinformation.md">FltReleaseFileNameInformation</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-iogettoplevelirp.md">IoGetTopLevelIrp</a>
</dt>
<dt>
<a href="..\fltkernel\nc-fltkernel-pflt_post_operation_callback.md">PFLT_POST_OPERATION_CALLBACK</a>
</dt>
<dt>
<a href="..\fltkernel\nc-fltkernel-pflt_pre_operation_callback.md">PFLT_PRE_OPERATION_CALLBACK</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FltGetFileNameInformation routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>