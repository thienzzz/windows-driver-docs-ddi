---
UID : NF:hbaapi.HBA_RemoveAllPersistentBindings
title : HBA_RemoveAllPersistentBindings function
author : windows-driver-content
description : The HBA_RemoveAllPersistentBindings routine removes all persistent bindings for a specified HBA port.
old-location : storage\hba_removeallpersistentbindings.htm
old-project : storage
ms.assetid : f15823dd-a9c5-46a8-a376-41b831450b66
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : HBA_RemoveAllPersistentBindings
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
req.alt-api : HBA_RemoveAllPersistentBindings
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


# HBA_RemoveAllPersistentBindings function
The <b>HBA_RemoveAllPersistentBindings</b> routine removes all persistent bindings for a specified HBA port.

## Syntax

````
HBA_STATUS HBA_API HBA_RemoveAllPersistentBindings(
  _In_ HBA_HANDLE Handle,
  _In_ HBA_WWN    HbaPortWWN
);
````

## Parameters

`Handle`

Contains a value returned by the routine <a href="..\hbaapi\nf-hbaapi-hba_openadapter.md">HBA_OpenAdapter</a> that identifies the HBA on which the port is located.

`HbaPortWWN`

Contains a 64-bit worldwide name (WWN) that uniquely identifies the local HBA port for which to remove all persistent bindings. For a discussion of worldwide names, see the T11 committee's <i>Fibre Channel HBA API</i> specification.


## Return Value

The <b>HBA_RemoveAllPersistentBindings</b> routine returns a value of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a> that indicates the status of the HBA. In particular, <b>HBA_RemoveAllPersistentBindings</b> returns one of the following values.
<dl>
<dt><b>HBA_STATUS_OK</b></dt>
</dl>Returned if all persistent bindings were successfully removed for the indicated port. 
<dl>
<dt><b>HBA_STATUS_ERROR_ILLEGAL_WWN</b></dt>
</dl>Returned if the HBA referenced by <i>handle</i> does not contain a port with a name that matches <i>HbaPortWWN</i>. 
<dl>
<dt><b>HBA_STATUS_ERROR_NOT_SUPPORTED</b></dt>
</dl>Returned if the HBA referenced by <i>handle</i> does not support persistent bindings.
<dl>
<dt><b>HBA_STATUS_ERROR</b></dt>
</dl>Returned if an unspecified error occurred that prevented the removal of the persistent bindings.

## Remarks

The removal of persistent bindings does not change target mappings until the operating system is restarted or HBA and/or fabric is reinitialized.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557233">HBA_STATUS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20HBA_RemoveAllPersistentBindings routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>