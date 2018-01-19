---
UID : NF:d3dkmthk.D3DKMTGetContextInProcessSchedulingPriority
title : D3DKMTGetContextInProcessSchedulingPriority function
author : windows-driver-content
description : Called by an in-process (in-proc) Microsoft Direct3D composition device to retrieve the scheduling priority for a device context that is in the same process as other device contexts.
old-location : display\d3dkmtgetcontextinprocessschedulingpriority.htm
old-project : display
ms.assetid : e2a662b6-6a16-4e63-b5a8-5701a7180f60
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3DKMTGetContextInProcessSchedulingPriority
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : d3dkmthk.h
req.include-header : D3dkmthk.h
req.target-type : Universal
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMTGetContextInProcessSchedulingPriority
req.alt-loc : D3dkmthk.h
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
req.typenames : D3DKMT_DRIVERVERSION
---


# D3DKMTGetContextInProcessSchedulingPriority function
Called by an in-process (in-proc) Microsoft Direct3D composition device to retrieve the scheduling priority for a device context that is in the same process as other device contexts.

## Syntax

````
_Check_return_ NTSTATUS APIENTRY D3DKMTGetContextInProcessSchedulingPriority(
  _Inout_ D3DKMT_GETCONTEXTINPROCESSSCHEDULINGPRIORITY *pContextPriority
);
````

## Parameters

This function has no parameters.

## Return Value

Returns one of the following values:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The scheduling priority was successfully retrieved.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>Parameters were validated and determined to be incorrect.

 

This function might also return other NTSTATUS values.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h (include D3dkmthk.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\d3dkmthk\ns-d3dkmthk-_d3dkmt_getcontextinprocessschedulingpriority.md">D3DKMT_GETCONTEXTINPROCESSSCHEDULINGPRIORITY</a>
</dt>
<dt>
<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtsetcontextinprocessschedulingpriority.md">D3DKMTSetContextInProcessSchedulingPriority</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMTGetContextInProcessSchedulingPriority function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>