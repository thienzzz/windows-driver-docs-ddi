---
UID : NF:ntifs.ZwQuerySecurityObject
title : ZwQuerySecurityObject function
author : windows-driver-content
description : The ZwQuerySecurityObject routine retrieves a copy of an object's security descriptor.
old-location : kernel\zwquerysecurityobject.htm
old-project : kernel
ms.assetid : bc3c494d-890c-4699-a272-62cbcc234cdd
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : ZwQuerySecurityObject
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available in Windows XP and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ZwQuerySecurityObject,NtQuerySecurityObject
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : PowerIrpDDis, HwStorPortProhibitedDDIs
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


# ZwQuerySecurityObject function
The <b>ZwQuerySecurityObject</b> routine retrieves a copy of an object's security descriptor.

## Syntax

````
NTSTATUS ZwQuerySecurityObject(
  _In_  HANDLE               Handle,
  _In_  SECURITY_INFORMATION SecurityInformation,
  _Out_ PSECURITY_DESCRIPTOR SecurityDescriptor,
  _In_  ULONG                Length,
  _Out_ PULONG               LengthNeeded
);
````

## Parameters

`Handle`

Handle for the object whose security descriptor is to be queried. This handle must have the access specified in the Meaning column of the table shown in the description of the <i>SecurityInformation</i> parameter.

`SecurityInformation`

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> value specifying the information to be queried.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DACL_SECURITY_INFORMATION

</td>
<td>
Indicates the discretionary access control list (DACL) of the object is being queried. Requires READ_CONTROL access. 

</td>
</tr>
<tr>
<td>
GROUP_SECURITY_INFORMATION

</td>
<td>
Indicates the primary group identifier of the object is being queried. Requires READ_CONTROL access. 

</td>
</tr>
<tr>
<td>
OWNER_SECURITY_INFORMATION

</td>
<td>
Indicates the owner identifier of the object is being queried. Requires READ_CONTROL access. 

</td>
</tr>
<tr>
<td>
SACL_SECURITY_INFORMATION

</td>
<td>
Indicates the system ACL (SACL) of the object is being queried. Requires ACCESS_SYSTEM_SECURITY access. 

</td>
</tr>
</table>

`SecurityDescriptor`

Caller-allocated buffer that <b>ZwQuerySecurityObject</b> fills with a copy of the specified security descriptor. The <a href="..\ntifs\ns-ntifs-_security_descriptor.md">SECURITY_DESCRIPTOR</a> structure is returned in self-relative format.

`Length`

Size, in bytes, of the buffer pointed to by <i>SecurityDescriptor</i>.

`LengthNeeded`

Pointer to a caller-allocated variable that receives the number of bytes required to store the copied security descriptor.


## Return Value

<b>ZwQuerySecurityObject</b> returns STATUS_SUCCESS or an appropriate error status. Possible error status codes include the following:
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl><i>Handle</i> did not have the required access. 
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>The buffer is too small for the security descriptor. None of the security information was copied to the buffer. 
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl><i>Handle</i> was not a valid handle. 
<dl>
<dt><b>STATUS_OBJECT_TYPE_MISMATCH</b></dt>
</dl><i>Handle</i> was not a handle of the expected type.

## Remarks

A security descriptor can be in absolute or self-relative form. In self-relative form, all members of the structure are located contiguously in memory. In absolute form, the structure only contains pointers to the members. 

The NTFS file system imposes a 64K limit on the size of the security descriptor that is written to disk for a file. (The FAT file system does not support security descriptors for files.) Thus a 64K <i>SecurityDescriptor</i> buffer is guaranteed to be large enough to hold the returned <b>SECURITY_DESCRIPTOR</b> structure. 

For more information about security and access control, see the documentation on these topics in the Windows SDK.

Minifilters should call <a href="..\fltkernel\nf-fltkernel-fltquerysecurityobject.md">FltQuerySecurityObject</a> instead of <b>ZwQuerySecurityObject</b>. 

For calls from kernel-mode drivers, the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a Windows Native System Services routine can behave differently in the way that they handle and interpret input parameters. For more information about the relationship between the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a routine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>.

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
| **DDI compliance rules** | PowerIrpDDis, HwStorPortProhibitedDDIs |

## See Also

<dl>
<dt>
<a href="..\fltkernel\nf-fltkernel-fltquerysecurityobject.md">FltQuerySecurityObject</a>
</dt>
<dt>
<a href="..\ntifs\ns-ntifs-_security_descriptor.md">SECURITY_DESCRIPTOR</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-zwsetsecurityobject.md">ZwSetSecurityObject</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ZwQuerySecurityObject routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>