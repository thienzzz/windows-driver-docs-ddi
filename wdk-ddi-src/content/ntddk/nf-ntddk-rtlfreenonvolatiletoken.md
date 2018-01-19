---
UID : NF:ntddk.RtlFreeNonVolatileToken
title : RtlFreeNonVolatileToken function
author : windows-driver-content
description : The routine RtlFreeNonVolatileToken is a cleanup function for the opaque NvToken which is given by a successful call to RtlGetNonVolatileToken.
old-location : ifsk\rtlfreenonvolatiletoken.htm
old-project : ifsk
ms.assetid : 8E083814-7408-47D2-A811-2DCBDCD13097
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RtlFreeNonVolatileToken
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntddk.h
req.include-header : Winnt.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10, version 1703
req.target-min-winversvr : None supported
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlFreeNonVolatileToken
req.alt-loc : ntddk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---


# RtlFreeNonVolatileToken function
The routine <b>RtlFreeNonVolatileToken</b> is a cleanup function for the opaque <b>NvToken</b> which is given by a successful
    call to <a href="..\ntddk\nf-ntddk-rtlgetnonvolatiletoken.md">RtlGetNonVolatileToken</a>.

## Syntax

````
NTSTATUS RtlFreeNonVolatileToken(
  _In_ PVOID NvToken
);
````

## Parameters

`NvToken`

A pointer to an opaque structure that has
        information about various properties of the non-volatile memory region which <a href="..\ntddk\nf-ntddk-rtlgetnonvolatiletoken.md">RtlGetNonVolatileToken</a> had returned.


## Return Value

The routine <b>RtlFreeNonVolatileToken</b> returns one of the status codes:
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl><b>NvToken</b> is an invalid pointer or token.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The request was successful.

## Remarks

This routine is currently not supported for Windows Server until the next major release of Windows Server.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Winnt.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/EA1C2DF3-591C-407A-ABBF-DE615466A498">RtlDrainNonVolatileFlush</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/759CDFAA-D939-44E7-AE03-E3ED90F8E09D">
RtlFlushNonVolatileMemory</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/169C5F41-B372-4056-AAC5-53DD0582A563">RtlFlushNonVolatileMemoryRanges</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/A9E866D4-C47F-4926-A838-EDB739CF1185">RtlGetNonVolatileToken</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/49DDDEF8-F949-4674-A18B-9BB091D163C2">RtlWriteNonVolatileMemory</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RtlFreeNonVolatileToken routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>