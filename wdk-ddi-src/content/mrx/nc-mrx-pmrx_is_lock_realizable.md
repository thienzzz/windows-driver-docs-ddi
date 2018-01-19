---
UID : NC:mrx.PMRX_IS_LOCK_REALIZABLE
title : PMRX_IS_LOCK_REALIZABLE
author : windows-driver-content
description : The MRxIsLockRealizable routine is called by RDBSS to request that a network mini-redirector indicate whether a specific byte-range lock is supported on this NET_ROOT structure.
old-location : ifsk\mrxislockrealizable.htm
old-project : ifsk
ms.assetid : 4b8c9a94-a81e-4a02-b68c-10b2fb64157f
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : _SetDSMCounters_IN, SetDSMCounters_IN, *PSetDSMCounters_IN
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : mrx.h
req.include-header : Mrx.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : MRxIsLockRealizable
req.alt-loc : mrx.h
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
req.typenames : SetDSMCounters_IN, *PSetDSMCounters_IN
---


# PMRX_IS_LOCK_REALIZABLE callback function
The<i> MRxIsLockRealizable</i> routine is called by <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/ifs/the-rdbss-driver-and-library">RDBSS</a> to request that a network mini-redirector indicate whether a specific byte-range lock is supported on this NET_ROOT structure.

## Syntax

```
PMRX_IS_LOCK_REALIZABLE PmrxIsLockRealizable;

NTSTATUS PmrxIsLockRealizable(
  IN OUT PMRX_FCB Fcb,
  IN PLARGE_INTEGER ByteOffset,
  IN PLARGE_INTEGER Length,
  IN ULONG LowIoLockFlags
)
{...}
```

## Parameters

`Fcb`



`ByteOffset`

A value indicating the byte offset for the byte range lock.

`Length`

A value indicating the length for the byte range lock.

`LowIoLockFlags`

A value indicating the I/O lock flags. This parameter is a bitmask that contains any combination of the following values:


## Return Value

<i>MRxIsLockRealizable</i> returns STATUS_SUCCESS on success or an appropriate NTSTATUS value, such as the following: 
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>The byte range lock that is requested is not supported. A network mini-redirector would return this value for a lock request that is not supported even if other types of byte range locks are supported. Unsupported locks might include 64-bit locks (the <b>ByteOffset-&gt;HighPart</b> member is nonzero), zero-length locks (the <b>Length</b> parameter is zero), or shared locks (the LOWIO_LOCKSFLAG_EXCLUSIVELOCK bit of the <i>LowIoLockFlags</i> parameter is not set).

## Remarks

<i>MRxIsLockRealizable</i> determines whether the specific byte-range lock requested is supported on this NET_ROOT structure. A network mini-redirector might support certain byte range locks and not support others. For example, a network mini-redirector might only support 32-bit byte range locks or exclusive locks.

<i>MRxIsLockRealizable</i> is called in response to receiving an IRP with the IRP_MN_LOCK minor function.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | mrx.h (include Mrx.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\mrx\nc-mrx-pmrx_chkfcb_calldown.md">MRxAreFilesAliased</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549841">MRxCleanupFobx</a>
</dt>
<dt>
<a href="..\mrx\nc-mrx-pmrx_calldown.md">MRxCloseSrvOpen</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549847">MRxCollapseOpen</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549862">MRxCreate</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549871">MRxDeallocateForFcb</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549872">MRxDeallocateForFobx</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549878">MRxExtendForCache</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549879">MRxExtendForNonCache</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550669">MRxFlush</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550677">MRxForceClosed</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550817">MRxShouldTryToCollapseThisOpen</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550839">MRxTruncate</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550844">MRxZeroExtend</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20MRxIsLockRealizable routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>