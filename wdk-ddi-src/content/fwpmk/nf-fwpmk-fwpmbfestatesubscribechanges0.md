---
UID : NF:fwpmk.FwpmBfeStateSubscribeChanges0
title : FwpmBfeStateSubscribeChanges0 function
author : windows-driver-content
description : The FwpmBfeStateSubscribeChanges0 function registers a callback function that is called whenever there is a change to the state of the filter engine.Note  FwpmBfeStateSubscribeChanges0 is a specific version of FwpmBfeStateSubscribeChanges.
old-location : netvista\fwpmbfestatesubscribechanges0.htm
old-project : netvista
ms.assetid : 375af8a1-9e05-4830-9074-6313b4e082d9
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FwpmBfeStateSubscribeChanges0
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : fwpmk.h
req.include-header : Fwpmk.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FwpmBfeStateSubscribeChanges0
req.alt-loc : fwpkclnt.lib,fwpkclnt.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Fwpkclnt.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : PINSTANCE_PARTIAL_INFORMATION, INSTANCE_PARTIAL_INFORMATION
---


# FwpmBfeStateSubscribeChanges0 function
The 
  <b>FwpmBfeStateSubscribeChanges0</b> function registers a callback function that is called whenever there is
  a change to the state of the filter engine.

## Syntax

````
NTSTATUS NTAPI FwpmBfeStateSubscribeChanges0(
  _Inout_  void                                *deviceObject,
  _In_     FWPM_SERVICE_STATE_CHANGE_CALLBACK0 callback,
  _In_opt_ void                                *context,
  _Out_    HANDLE                              *changeHandle
);
````

## Parameters

`deviceObject`

A pointer to a device object that was previously created by the callout driver. For more
     information about how a callout driver creates a device object, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff542862">Creating a Device Object</a>.

`callback`

A pointer to a callout driver-provided service state change callback function. The filter engine
     calls this function whenever there is a change in the state of the filter engine.
     

A service-state-change callback function is declared as follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>VOID NTAPI
callback(
    IN OUT void  *context,
    IN FWPM_SERVICE_STATE  newState
    );</pre>
</td>
</tr>
</table></span></div>

`context`

A pointer to a callout driver-provided context that is passed to the callback function specified
     in the 
     <i>Callback</i> parameter.

`changeHandle`

A pointer to a variable that receives a handle that is associated with the registration of the
     callback function. A callout driver passes this handle to the
     <a href="..\fwpmk\nf-fwpmk-fwpmbfestateunsubscribechanges0.md">FwpmBfeStateUnsubscribeChanges0</a> function to deregister the callback function.


## Return Value

The 
     <b>FwpmBfeStateSubscribeChanges0</b> function returns one of the following NTSTATUS codes:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The callback function was successfully registered.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

A callout driver calls the 
    <b>FwpmBfeStateSubscribeChanges0</b> function to register a callback function that is called whenever
    there is a change to the state of the filter engine. 

For example, a callout driver cannot open a session to the filter
    engine by calling  the <a href="..\fwpmk\nf-fwpmk-fwpmengineopen0.md">FwpmEngineOpen0</a> function unless the filter engine is currently running. A callout driver can use the <b>FWPM_SERVICE_RUNNING</b>
    notification to open a session to the filter engine so that it can make calls to the other Windows
    Filtering Platform 
    <a href="https://answers.microsoft.com/en-us/windows/forum/windows_xp-performance/computer-management-storage-disk-management/f93a4e9b-5516-4e5c-9cd3-f04453ec963f">management functions</a>. Similarly, a
    callout driver can use the <b>FWPM_SERVICE_STOP_PENDING</b> notification to perform any cleanup before the
    filter engine is stopped.

A callout driver must call <b>FwpmBfeStateSubscribeChanges0</b> before calling the <a href="..\fwpmk\nf-fwpmk-fwpmbfestateget0.md">FwpmBfeStateGet0</a> function to retrieve the current state of the filter engine. After  the call to <b>FwpmBfeStateSubscribeChanges0</b> returns, the callout driver can call 
    <b>FwpmBfeStateGet0</b> at any time.

A callout driver must deregister the callback function by calling the 
    <a href="..\fwpmk\nf-fwpmk-fwpmbfestateunsubscribechanges0.md">
    FwpmBfeStateUnsubscribeChanges0</a> function before the callout driver can be unloaded.
<p class="note">Do not call <a href="..\fwpmk\nf-fwpmk-fwpmbfestateunsubscribechanges0.md">FwpmBfeStateUnsubscribeChanges0</a> from the callback function that you passed in the <i>callback</i> parameter. Doing so can cause a deadlock.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpmk.h (include Fwpmk.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\fwpmk\nf-fwpmk-fwpmbfestateget0.md">FwpmBfeStateGet0</a>
</dt>
<dt>
<a href="..\fwpmk\nf-fwpmk-fwpmbfestateunsubscribechanges0.md">
   FwpmBfeStateUnsubscribeChanges0</a>
</dt>
<dt>
<a href="..\fwpmk\nf-fwpmk-fwpmengineopen0.md">FwpmEngineOpen0</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FwpmBfeStateSubscribeChanges0 function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>