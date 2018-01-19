---
UID : NF:hbaapi.HBA_RegisterForAdapterPortEvents
title : HBA_RegisterForAdapterPortEvents function
author : windows-driver-content
description : The HBA_RegisterForAdapterPortEvents routine registers the indicated user callback routine to call when a port event occurs.
old-location : storage\hba_registerforadapterportevents.htm
old-project : storage
ms.assetid : 596bfba5-7025-4cdc-b1f9-c8df546f6dac
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : HBA_RegisterForAdapterPortEvents
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : hbaapi.h
req.include-header : Hbaapi.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : HBA_RegisterForAdapterPortEvents
req.alt-loc : Hbaapi.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Hbaapi.lib
req.dll : Hbaapi.dll
req.irql : 
req.typenames : HBA_WWNTYPE
---


# HBA_RegisterForAdapterPortEvents function
The <b>HBA_RegisterForAdapterPortEvents</b> routine registers the indicated user callback routine to call when a port event occurs.

## Syntax

````
HBA_STATUS HBA_API HBA_RegisterForAdapterPortEvents(
   HBA_PORT_CALLBACK  callback,
   void               *userData,
   HBA_HANDLE         handle,
   HBA_WWN            PortWWN,
   HBA_CALLBACKHANDLE *callbackHandle
);
````

## Parameters

`callback`

Pointer to a callback routine of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff557123">HBA_PORT_CALLBACK</a> that is called when an adapter is added to the system.

`UserData`



`Handle`



`PortWWN`

Contains a 64-bit worldwide name (WWN) that uniquely identifies the HBA port from which port events are reported. For a discussion of worldwide names, see the T11 committee's <i>Fibre Channel HBA API</i> specification.

`pCallbackHandle`




## Return Value

The <b>HBA_RegisterForAdapterPortEvents</b> routine returns a value of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a> that indicates the status of the HBA. In particular, this member should have one of the following values.
<dl>
<dt><b>HBA_STATUS_OK</b></dt>
</dl>Returned if the callback routine was successfully registered. 
<dl>
<dt><b>HBA_STATUS_ERROR_ILLEGAL_WWN</b></dt>
</dl>Returned if the HBA referenced by <i>handle</i> does not have a port with a name that matches the value in <i>PortWWN</i>.
<dl>
<dt><b>HBA_STATUS_ERROR</b></dt>
</dl>Returned if an unspecified error occurred that prevented the registration of the callback routine.

## Remarks

For a list of port events, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff557123">HBA_PORT_CALLBACK</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbaapi.h (include Hbaapi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\hbaapi\nf-hbaapi-hba_openadapter.md">HBA_OpenAdapter</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557123">HBA_PORT_CALLBACK</a>
</dt>
<dt>
<a href="..\hbaapi\nf-hbaapi-hba_removecallback.md">HBA_RemoveCallback</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20HBA_RegisterForAdapterPortEvents routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>