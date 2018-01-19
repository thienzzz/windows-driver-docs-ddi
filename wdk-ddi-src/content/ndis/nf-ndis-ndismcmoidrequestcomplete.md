---
UID : NF:ndis.NdisMCmOidRequestComplete
title : NdisMCmOidRequestComplete macro
author : windows-driver-content
description : The NdisMCmOidRequestComplete function returns the final status of a CoNDIS OID requestthat a miniport call manager (MCM) driver's ProtocolCoOidRequest function previously returned NDIS_STATUS_PENDING for.
old-location : netvista\ndismcmoidrequestcomplete.htm
old-project : netvista
ms.assetid : 4c45be9f-3d07-4150-830a-3aa6d74531ff
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisMCmOidRequestComplete
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : macro
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Desktop
req.target-min-winverclnt : Supported in NDIS 6.0 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisMCmOidRequestComplete
req.alt-loc : ndis.h
req.ddi-compliance : Irql_MCM_Function
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisMCmOidRequestComplete function
The 
  <b>NdisMCmOidRequestComplete</b> function returns the final status of a CoNDIS OID requestthat a miniport
  call manager (MCM) driver's 
  <a href="..\ndis\nc-ndis-protocol_co_oid_request.md">ProtocolCoOidRequest</a> function
  previously returned NDIS_STATUS_PENDING for.

## Syntax

````
VOID NdisMCmOidRequestComplete(
  [in]           NDIS_HANDLE       NdisAfHandle,
  [in, optional] NDIS_HANDLE       NdisVcHandle,
  [in, optional] NDIS_HANDLE       NdisPartyHandle,
  [in]           PNDIS_OID_REQUEST OidRequest,
  [in]           NDIS_STATUS       Status
);
````

## Parameters

`_AH_`



`_VH_`



`_PH_`



`_R_`



`_S_`




## Return Value

None

## Remarks

A CoNDIS MCM that returns NDIS_STATUS_PENDING from its 
    <a href="..\ndis\nc-ndis-protocol_co_oid_request.md">ProtocolCoOidRequest</a> function must
    call the 
    <b>NdisMCmOidRequestComplete</b> function after the MCM has finished the OID request operation.

After the MCM calls 
    <b>NdisMCmOidRequestComplete</b>, NDIS calls the 
    <a href="..\ndis\nc-ndis-protocol_co_oid_request_complete.md">
    ProtocolCoOidRequestComplete</a> function of the CoNDIS client that originally called the 
    <a href="..\ndis\nf-ndis-ndiscooidrequest.md">NdisCoOidRequest</a> function.

For more information about the OIDs defined to use with CONDIS drivers, see 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff566707">NDIS OIDs</a>.

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
| **DDI compliance rules** | Irql_MCM_Function |

## See Also

<dl>
<dt>
<a href="..\ndis\ns-ndis-_ndis_oid_request.md">NDIS_OID_REQUEST</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndiscooidrequest.md">NdisCoOidRequest</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_co_oid_request.md">ProtocolCoOidRequest</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_co_oid_request_complete.md">
   ProtocolCoOidRequestComplete</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisMCmOidRequestComplete macro%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>