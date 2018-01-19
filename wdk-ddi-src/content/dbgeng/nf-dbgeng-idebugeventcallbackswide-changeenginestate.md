---
UID : NF:dbgeng.IDebugEventCallbacksWide.ChangeEngineState
title : IDebugEventCallbacksWide::ChangeEngineState method
author : windows-driver-content
description : The ChangeEngineState callback method is called by the engine when its state has changed.
old-location : debugger\idebugeventcallbackswide_changeenginestate.htm
old-project : debugger
ms.assetid : 14205476-3f58-4105-99a7-a3baa2eba033
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugEventCallbacksWide, IDebugEventCallbacksWide::ChangeEngineState, ChangeEngineState
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugEventCallbacksWide.ChangeEngineState
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


# ChangeEngineState method
The <b>ChangeEngineState</b> callback method is called by the engine when its state has changed.

## Syntax

````
HRESULT ChangeEngineState(
  [in] ULONG   Flags,
  [in] ULONG64 Argument
);
````

## Parameters

`Flags`

Specifies a bit-set indicating the type of changes that occurred in the engine's state.  The following bit flags might be set:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
DEBUG_CES_CURRENT_THREAD

</td>
<td>
The current thread has changed, which implies that the current target and current process might also have changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_EFFECTIVE_PROCESSOR

</td>
<td>
The effective processor has changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_BREAKPOINTS

</td>
<td>
One or more <a href="debugger.multiprocessor_syntax#breakpoints#breakpoints">breakpoints</a> have changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_CODE_LEVEL

</td>
<td>
The code interpretation level has changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_EXECUTION_STATUS

</td>
<td>
The execution status has changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_ENGINE_OPTIONS

</td>
<td>
The engine options have changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_LOG_FILE

</td>
<td>
The log file has been opened or closed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_RADIX

</td>
<td>
The default radix has changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_EVENT_FILTERS

</td>
<td>
The event filters have changed.  

</td>
</tr>
<tr>
<td>
DEBUG_CES_PROCESS_OPTIONS

</td>
<td>
The process options for the current process have changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_EXTENSIONS

</td>
<td>
Extension DLLs have been loaded or unloaded. (For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552040">Loading Debugger Extension DLLs</a>.)

</td>
</tr>
<tr>
<td>
DEBUG_CES_SYSTEMS

</td>
<td>
A target has been added or removed.  

</td>
</tr>
<tr>
<td>
DEBUG_CES_ASSEMBLY_OPTIONS

</td>
<td>
The assemble options have changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_EXPRESSION_SYNTAX

</td>
<td>
The default expression syntax has changed.

</td>
</tr>
<tr>
<td>
DEBUG_CES_TEXT_REPLACEMENTS

</td>
<td>
Text replacements have changed.  

</td>
</tr>
</table>

`Argument`

Provides additional information about the change to the engine's state.  If more than one bit flag is set in the <i>Flags</i> parameter, the <i>Argument</i> parameter is not used.  Otherwise, the interpretation of the value of <i>Argument</i> depends on the value of <i>Flags</i>:


## Return Value

The return value is ignored by the engine unless it indicates a remote procedure call error; in this case the client, with which this <b>IDebugEventCallbacksWide</b> object is registered, is disabled.

## Remarks

This method is only called by the engine if the DEBUG_EVENT_CHANGE_ENGINE_STATE flag is set in the mask returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff550625">IDebugEventCallbacksWide::GetInterestMask</a>.

For more information about handling events, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552239">Monitoring Events</a>. </p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |