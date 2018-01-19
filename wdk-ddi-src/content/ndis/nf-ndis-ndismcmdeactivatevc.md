---
UID : NF:ndis.NdisMCmDeactivateVc
title : NdisMCmDeactivateVc function
author : windows-driver-content
description : NdisMCmDeactivateVc notifies NDIS that there will be no further transfers on a particular active VC.
old-location : netvista\ndismcmdeactivatevc.htm
old-project : netvista
ms.assetid : e18f6326-621e-4bed-aa82-b326f3b1422d
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisMCmDeactivateVc
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Desktop
req.target-min-winverclnt : Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisMCmDeactivateVc (NDIS   5.1)) in Windows Vista. Supported for NDIS 5.1 drivers (see    NdisMCmDeactivateVc (NDIS   5.1)) in Windows XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisMCmDeactivateVc
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : Irql_MCM_Function
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


# NdisMCmDeactivateVc function
<b>NdisMCmDeactivateVc</b> notifies NDIS that there will be no further transfers on a particular active
  VC.

## Syntax

````
NDIS_STATUS NdisMCmDeactivateVc(
  _In_ NDIS_HANDLE NdisVcHandle
);
````

## Parameters

`NdisVcHandle`

Specifies the handle identifying the VC. This handle was supplied by NDIS to the MCM driver either
     when it called 
     <a href="..\ndis\nf-ndis-ndismcmcreatevc.md">NdisMCmCreateVc</a> for an incoming call or
     when its 
     <a href="..\ndis\nc-ndis-protocol_co_create_vc.md">ProtocolCoCreateVc</a> function set up
     the VC for a client-initiated outgoing call.


## Return Value

<b>NdisMCmDeactivateVc</b> can return one of the following:
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>NDIS marked the VC as inactive.
<dl>
<dt><b>NDIS_STATUS_NOT_ACCEPTED</b></dt>
</dl>The VC is already deactivated, so this call is redundant.

## Remarks

An MCM driver calls 
    <b>NdisMCmDeactivateVc</b> as an essential step in closing a call, usually after the packet exchange with
    network components that tears down the connection.

A successful call to 
    <b>NdisMCmDeactivateVc</b> allows the MCM driver to discard the current call parameters for transfers on
    the VC, possibly reinitializing them to miniport driver-determined default values. However, if the VC is
    reactivated subsequently for another call, the client will supply new call parameters to the miniport
    driver.

The 
    <i>NdisVcHandle</i> passed to 
    <b>NdisMCmDeactivateVc</b> remains valid after VC deactivation is completed. The deactivation of any VC
    allows its creator to reinitialize the VC for reuse or to destroy it:

Following VC deactivation and the closing of the call, a client can reuse a VC that it originally
      created to make another call with 
      <a href="..\ndis\nf-ndis-ndisclmakecall.md">NdisClMakeCall</a>, or it can call 
      <a href="..\ndis\nf-ndis-ndiscodeletevc.md">NdisCoDeleteVc</a>, thereby causing a call
      to the MCM driver's 
      <a href="..\ndis\nc-ndis-protocol_co_delete_vc.md">ProtocolCoDeleteVc</a> function.

Following VC deactivation and the closing of the call, an MCM driver can reuse a VC that it
      originally created to indicate another incoming call to the same client with 
      <a href="..\ndis\nf-ndis-ndismcmdispatchincomingcall.md">
      NdisMCmDispatchIncomingCall</a>, or it can call 
      <a href="..\ndis\nf-ndis-ndismcmdeletevc.md">NdisMCmDeleteVc</a>.

The driver writer determines whether an MCM driver has an (internal) 
    <i>MiniportCoDeactivateVc</i> function that the driver calls in the context of tearing down connections
    for outgoing and incoming calls.

Only connection-oriented miniport drivers that provide integrated call-management support can call 
    <b>NdisMCmDeactivateVc</b>. Stand-alone call managers, which register themselves with NDIS as protocol
    drivers, call 
    <b>NdisCmDeactivateVc</b> instead.

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
<a href="..\ndis\nc-ndis-miniport_co_deactivate_vc.md">MiniportCoDeactivateVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisclclosecall.md">NdisClCloseCall</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisclmakecall.md">NdisClMakeCall</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndiscmdeactivatevc.md">NdisCmDeactivateVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismcmactivatevc.md">NdisMCmActivateVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismcmdeletevc.md">NdisMCmDeleteVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismcmdispatchincomingcall.md">NdisMCmDispatchIncomingCall</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_cm_close_call.md">ProtocolCmCloseCall</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_co_delete_vc.md">ProtocolCoDeleteVc</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisMCmDeactivateVc function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>