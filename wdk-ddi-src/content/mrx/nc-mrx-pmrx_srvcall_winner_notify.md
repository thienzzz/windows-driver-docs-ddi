---
UID : NC:mrx.PMRX_SRVCALL_WINNER_NOTIFY
title : PMRX_SRVCALL_WINNER_NOTIFY
author : windows-driver-content
description : The MRxSrvCallWinnerNotify routine is called by RDBSS to notify a network mini-redirector that it was chosen when multiple redirectors could fulfill the request.
old-location : ifsk\mrxsrvcallwinnernotify.htm
old-project : ifsk
ms.assetid : 6853b73e-5516-485e-ade4-54b7faf6bb1d
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
req.alt-api : MRxSrvCallWinnerNotify
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


# PMRX_SRVCALL_WINNER_NOTIFY callback function
The<i> MRxSrvCallWinnerNotify</i> routine is called by <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/ifs/the-rdbss-driver-and-library">RDBSS</a> to notify a network mini-redirector that it was chosen when multiple redirectors could fulfill the request.

## Syntax

```
PMRX_SRVCALL_WINNER_NOTIFY PmrxSrvcallWinnerNotify;

NTSTATUS PmrxSrvcallWinnerNotify(
  IN OUT PMRX_SRV_CALL SrvCall,
  IN BOOLEAN ThisMinirdrIsTheWinner,
  IN OUT PVOID RecommunicateContext
)
{...}
```

## Parameters

`SrvCall`



`ThisMinirdrIsTheWinner`

A Boolean value that indicates that this network mini-redirector was chosen.

`RecommunicateContext`




## Return Value

<i>MRxSmbSrvCallWinnerNotify</i> returns STATUS_SUCCESS on success.

## Remarks

<i>MRxSrvCallWinnerNotify</i> was originally designed to be called by RDBSS to notify a network mini-redirector that it was chosen when multiple redirectors could fulfill the request. The chosen network mini-redirector is expected to create the SRV_CALL structure and establish a connection with the server.

The network mini-redirector should complete the context for the SRV_CALL structure. If the network mini-redirector supports case-insensitive names for NET_ROOT structures and for filenames, then the SRV_CALL <b>Flags</b> member should set the bits for SRVCALL_FLAG_CASE_INSENSITIVE_NETROOTS and SRVCALL_FLAG_CASE_INSENSITIVE_FILENAMES.

Under the current implementation of RDBSS, each network mini-redirector has its own copy of RDBSS, so there are no competing network redirectors at the RDBSS layer. All network mini-redirectors will receive a call to <i>MRxSrvCallWinnerNotify</i> with the <i>ThisMinirdrIsTheWinner</i> parameter set to <b>TRUE</b> after receiving a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff549864">MRxCreateSrvCall</a> to create the SRV_CALL structure. 

When multiple redirectors are installed for handling the same UNC namespace, the redirector to service a request is chosen by multiple UNC provider (MUP) based on the order of redirectors specified in the registry.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549864">MRxCreateSrvCall</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549869">MRxCreateVNetRoot</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550649">MRxExtractNetRootName</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550653">MRxFinalizeNetRoot</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550663">MRxFinalizeVNetRoot</a>
</dt>
<dt>
<a href="..\fcb\nf-fcb-rxfinalizesrvcall.md">RxFinalizeSrvCall</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550750">MRxPreparseName</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20MRxSrvCallWinnerNotify routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>