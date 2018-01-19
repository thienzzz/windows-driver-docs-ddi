---
UID : NF:midatlax.RxReassociateMid
title : RxReassociateMid function
author : windows-driver-content
description : RxReassociateMid reassociates a Multiplex ID (MID) with an alternate context.
old-location : ifsk\rxreassociatemid.htm
old-project : ifsk
ms.assetid : 2b80aa77-45b3-4157-8ab5-770c827a536a
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RxReassociateMid
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : midatlax.h
req.include-header : Midatlax.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RxReassociateMid
req.alt-loc : midatlax.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= APC_LEVEL
req.typenames : MCD_INIT_DATA, *PMCD_INIT_DATA
---


# RxReassociateMid function
<b>RxReassociateMid</b> reassociates a Multiplex ID (MID) with an alternate context.

## Syntax

````
NTSTATUS RxReassociateMid(
   PRX_MID_ATLAS pMidAtlas,
   USHORT        Mid,
   PVOID         pNewContext
);
````

## Parameters

`MidAtlas`



`Mid`

The multiplex ID to be mapped.

`NewContext`




## Return Value

<b>RxReassociateMid</b> returns STATUS_SUCCESS on success. The returned <i>pNewMid</i> parameter can be <b>NULL</b> if no context is associated with this MID.

## Remarks

RDBSS defines a MID as a 16-bit value, which can be used by both the network client (mini-redirector) and the server to distinguish between the concurrently active requests on any connection. A MID is a component of a MID_ATLAS data structure allocated by calling <a href="..\midatlax\nf-midatlax-rxcreatemidatlas.md">RxCreateMidAtlas</a>. A MID_MAP data structure is allocated and used for mapping MIDs to RX_CONTEXT data structures.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | midatlax.h (include Midatlax.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\midatlax\nf-midatlax-rxassociatecontextwithmid.md">RxAssociateContextWithMid</a>
</dt>
<dt>
<a href="..\midatlax\nf-midatlax-rxcreatemidatlas.md">RxCreateMidAtlas</a>
</dt>
<dt>
<a href="..\midatlax\nf-midatlax-rxdestroymidatlas.md">RxDestroyMidAtlas</a>
</dt>
<dt>
<a href="..\midatlax\nf-midatlax-rxmapmidtocontext.md">RxMapMidToContext</a>
</dt>
<dt>
<a href="..\midatlax\nf-midatlax-rxmapanddissociatemidfromcontext.md">RxMapAndDissociateMidFromContext</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RxReassociateMid function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>