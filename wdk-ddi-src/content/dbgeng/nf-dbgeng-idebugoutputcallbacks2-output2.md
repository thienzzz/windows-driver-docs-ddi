---
UID : NF:dbgeng.IDebugOutputCallbacks2.Output2
title : IDebugOutputCallbacks2::Output2 method
author : windows-driver-content
description : Returns notifications for the IDebugOutputCallbacks2 interface.
old-location : debugger\idebugoutputcallbacks2_output2.htm
old-project : debugger
ms.assetid : 2FFF9B54-6E77-4D46-B6C0-5BADD208BFCC
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugOutputCallbacks2, IDebugOutputCallbacks2::Output2, Output2
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugOutputCallbacks2.Output2
req.alt-loc : dbgeng.h
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
req.typenames : "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---


# Output2 method
Returns notifications for the <a href="..\dbgeng\nn-dbgeng-idebugoutputcallbacks2.md">IDebugOutputCallbacks2</a> interface.

## Syntax

````
HRESULT Output2(
  [in]           ULONG   Which,
  [in]           ULONG   Flags,
  [in]           ULONG64 Arg,
  [in, optional] PCWSTR  Text
);
````

## Parameters

`Which`

The kind of notification that is coming in. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>

`Flags`

Flags that are part of the notification payload.

`Arg`

Arguments that are part of the notification payload.

`Text`

A pointer to text that is part of the notification payload.


## Return Value

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugoutputcallbacks2.md">IDebugOutputCallbacks2</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugOutputCallbacks2::Output2 method%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>