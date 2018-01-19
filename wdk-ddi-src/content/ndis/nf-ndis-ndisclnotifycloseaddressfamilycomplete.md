---
UID : NF:ndis.NdisClNotifyCloseAddressFamilyComplete
title : NdisClNotifyCloseAddressFamilyComplete function
author : windows-driver-content
description : The NdisClNotifyCloseAddressFamilyComplete function returns the final status of an address family (AF) close operation for which the caller's ProtocolClNotifyCloseAf function returned NDIS_STATUS_PENDING.
old-location : netvista\ndisclnotifycloseaddressfamilycomplete.htm
old-project : netvista
ms.assetid : 5d2bbf08-ea5c-4dad-8c30-9a655d25222a
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisClNotifyCloseAddressFamilyComplete
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Desktop
req.target-min-winverclnt : Supported in NDIS 6.0 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisClNotifyCloseAddressFamilyComplete
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : Irql_Protocol_Driver_Function
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ndis.lib
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisClNotifyCloseAddressFamilyComplete function
The 
  <b>NdisClNotifyCloseAddressFamilyComplete</b> function returns the final status of an address family (AF)
  close operation for which the caller's 
  <a href="..\ndis\nc-ndis-protocol_cl_notify_close_af.md">ProtocolClNotifyCloseAf</a> function
  returned NDIS_STATUS_PENDING.

## Syntax

````
VOID NdisClNotifyCloseAddressFamilyComplete(
  _In_ NDIS_HANDLE NdisAfHandle,
  _In_ NDIS_STATUS Status
);
````

## Parameters

`NdisAfHandle`

An AF handle that NDIS supplied to the caller's 
     <a href="..\ndis\nf-ndis-ndisclopenaddressfamilyex.md">
     NdisClOpenAddressFamilyEx</a> function.

`Status`

The completion status for close AF notification.
     

<i>Status</i> can be one of the following:


## Return Value

None

## Remarks

CoNDIS clients call the 
    <b>NdisClNotifyCloseAddressFamilyComplete</b> function to complete a close AF notification. A client must
    call 
    <b>NdisClNotifyCloseAddressFamilyComplete</b> after its 
    <a href="..\ndis\nc-ndis-protocol_cl_notify_close_af.md">
    ProtocolClNotifyCloseAf</a> function returns NDIS_STATUS_PENDING.

After the client calls 
    <b>NdisClNotifyCloseAddressFamilyComplete</b>, NDIS calls the call manager's 
    <a href="..\ndis\nc-ndis-protocol_cm_notify_close_af_complete.md">
    ProtocolCmNotifyCloseAfComplete</a> function to complete operation for the call manager.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** | Irql_Protocol_Driver_Function |

## See Also

<dl>
<dt>
<a href="..\ndis\nf-ndis-ndisclopenaddressfamilyex.md">NdisClOpenAddressFamilyEx</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_cl_notify_close_af.md">ProtocolClNotifyCloseAf</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_cm_notify_close_af_complete.md">
   ProtocolCmNotifyCloseAfComplete</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisClNotifyCloseAddressFamilyComplete function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>