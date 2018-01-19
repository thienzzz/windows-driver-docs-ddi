---
UID : NF:ntifs.SecMakeSPNEx2
title : SecMakeSPNEx2 function
author : windows-driver-content
description : SecMakeSPNEx2 creates a service provider name string that can be used when it communicates with specific security service providers.
old-location : ifsk\secmakespnex2.htm
old-project : ifsk
ms.assetid : abb8d45a-a698-41b0-94b3-c658fe3105bb
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : SecMakeSPNEx2
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Ntifs.h, FltKernel.h
req.target-type : Universal
req.target-min-winverclnt : This function is available on Windows Vista, Windows Server 2008, and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : SecMakeSPNEx2
req.alt-loc : Ksecdd.lib,Ksecdd.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ksecdd.lib
req.dll : 
req.irql : <= APC_LEVEL
req.typenames : TOKEN_TYPE
---


# SecMakeSPNEx2 function
<b>SecMakeSPNEx2</b> creates a service provider name string that can be used when it communicates with specific security service providers.

## Syntax

````
NTSTATUS SecMakeSPNEx2(
  _In_    PUNICODE_STRING ServiceClass,
  _In_    PUNICODE_STRING ServiceName,
  _In_    PUNICODE_STRING InstanceName,
  _In_    USHORT          InstancePort,
  _In_    PUNICODE_STRING Referrer,
  _In_    PUNICODE_STRING TargetInfo,
  _Inout_ PUNICODE_STRING Spn,
  _Out_   PULONG          TotalSize,
  _In_    BOOLEAN         Allocate,
  _In_    BOOLEAN         IsTargetInfoMarshaled
);
````

## Parameters

`ServiceClass`

A pointer to a Unicode string that specifies the service class for the security service provider.

`ServiceName`

A pointer to a Unicode string that specifies the service name for the security service provider.

`OPTIONAL`



`OPTIONAL`



`OPTIONAL`



`OPTIONAL`



`Spn`

A pointer to a Unicode string that receives the security service provider name string that is created by this function.

`OPTIONAL`



`Allocate`

A Boolean variable that indicates if the memory that is used to store the <i>Spn</i> Unicode string should be allocated by this function. If this parameter is <b>TRUE</b>, memory for <i>Spn</i> will be allocated from paged pool.

`IsTargetInfoMarshaled`

A Boolean variable that indicates that the caller provided a marshaled <i>InTargetInfo</i> structure.  If <i>IsTargetInfoMarshaled</i> is <b>TRUE</b>, <i>InTargetInfo</i>-&gt;Buffer points to a string representation of the CREDENTIAL_TARGET_INFORMATION structure as returned by the <b>CredMarshalTargetInfo</b> function.


## Return Value

<b>SecMakeSPNEx2</b> returns STATUS_SUCCESS on success or one of the following error codes on failure: 
<dl>
<dt><b>STATUS_BUFFER_OVERFLOW</b></dt>
</dl>The <i>Allocate</i> parameter was set to <b>FALSE</b> and one of the following conditions occurred:

The <i>Spn </i>parameter was a <b>NULL</b> pointer.

The maximum length for the <i>Spn</i> Unicode string parameter was too small.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>A total length of the <i>Spn</i> parameter exceeds 65535 bytes.
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>The <i>Allocate</i> parameter was set to <b>TRUE</b>, but the memory allocation request failed.

## Remarks

<b>SecMakeSPNEx2</b> is an enhanced version of <b>SecMakeSPNEx</b>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Ntifs.h, FltKernel.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ntifs\nf-ntifs-secmakespn.md">SecMakeSPN</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-secmakespnex.md">SecMakeSPNEx</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20SecMakeSPNEx2 function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>