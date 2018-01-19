---
UID : NF:ndis.NdisMCmCreateVc
title : NdisMCmCreateVc function
author : windows-driver-content
description : NdisMCmCreateVc sets up a connection endpoint on which an MCM driver can dispatch an incoming-call offer to a client.
old-location : netvista\ndismcmcreatevc.htm
old-project : netvista
ms.assetid : b1d9ce90-9926-4ff8-a5bb-54c1a88d84dc
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisMCmCreateVc
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Desktop
req.target-min-winverclnt : Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisMCmCreateVc (NDIS 5.1)) in   Windows Vista. Supported for NDIS 5.1 drivers (see    NdisMCmCreateVc (NDIS 5.1)) in   Windows XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisMCmCreateVc
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


# NdisMCmCreateVc function
<b>NdisMCmCreateVc</b> sets up a connection endpoint on which an MCM driver can dispatch an incoming-call
  offer to a client.

## Syntax

````
NDIS_STATUS NdisMCmCreateVc(
  _In_  NDIS_HANDLE  MiniportAdapterHandle,
  _In_  NDIS_HANDLE  NdisAfHandle,
  _In_  NDIS_HANDLE  MiniportVcContext,
  _Out_ PNDIS_HANDLE NdisVcHandle
);
````

## Parameters

`MiniportAdapterHandle`

Specifies the NDIS-supplied handle originally input to 
     <a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a>.

`NdisAfHandle`

Specifies the handle that identifies the client that is the target of an incoming call. The MCM
     driver obtained this handle as an input parameter to its 
     <a href="..\ndis\nc-ndis-protocol_cm_open_af.md">ProtocolCmOpenAf</a> function.

`MiniportVcContext`

Specifies the handle to a caller-supplied resident context area in which the MCM driver maintains
     state for this VC. NDIS passes this handle back to the MCM driver in all subsequent calls concerning
     this VC if the call to 
     <b>NdisMCmCreateVc</b> succeeds.

`NdisVcHandle`

Pointer to a caller-supplied variable that must be initialized to <b>NULL</b> before 
     <b>NdisMCmCreateVc</b> is called. On return from a successful call, this variable has been set to an
     NDIS-supplied handle for the newly created VC. The caller must save this handle for subsequent calls to
     connection-oriented 
     <b>Ndis<i>Xxx</i></b> functions concerning this VC.


## Return Value

<b>NdisMCmCreateVc</b> can return one of the following:
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>NDIS created the VC successfully.
<dl>
<dt><b>NDIS_STATUS_RESOURCES</b></dt>
</dl>NDIS could not allocate sufficient memory to set up the VC.
<dl>
<dt><b>NDIS_STATUS_FAILURE</b></dt>
</dl>The given 
       <i>NdisAfHandle</i> is invalid.
<dl>
<dt><b>NDIS_STATUS_<i>XXX</i></b></dt>
</dl>The client failed the creation of the VC for some reason, and NDIS has propagated the error
       status returned by its 
       <a href="..\ndis\nc-ndis-protocol_co_create_vc.md">ProtocolCoCreateVc</a> function to
       the MCM driver.

## Remarks

An MCM driver creates a VC with 
    <b>NdisMCmCreateVc</b> to represent an incoming offer of a connection from a remote node directed to a SAP
    that has already been registered with the MCM driver.

In the process of VC creation, NDIS supplies an 
    <i>NdisVcHandle</i> to the client and the MCM driver. This handle identifies the virtual connection for
    the client and miniport driver to which subsequent requests concerning the given VC are directed. Each
    driver must treat this VC handle as an opaque variable, passing it unmodified and uninterpreted in
    subsequent calls to certain connection-oriented NDIS library functions.

Usually, callers of 
    <b>NdisMCmCreateVc</b> store the returned 
    <i>NdisVcHandle</i> in the caller-allocated state area at 
    <i>MiniportVcContext</i> . NDIS passes an 
    <i>NdisVcHandle</i> as an input parameter to the 
    <i>ProtocolCoCreateVc</i> function of the appropriate client whenever an MCM driver creates a VC.

When an MCM driver processes the offer of an incoming call directed to one of its registered SAPs, it
    must call 
    <b>NdisMCmCreateVc</b> first. As a synchronous operation, NDIS calls the client's 
    <i>ProtocolCoCreateVc</i> function before 
    <b>NdisMCmCreateVc</b> returns control. If its call to 
    <b>NdisMCmCreateVc</b> succeeds, the MCM driver can proceed in notifying the appropriate client, passing
    the returned value at 
    <i>NdisVcHandle</i> to 
    <a href="..\ndis\nf-ndis-ndismcmdispatchincomingcall.md">
    NdisMCmDispatchIncomingCall</a>.

The driver writer determines whether an MCM driver has an (internal) 
    <a href="..\ndis\nc-ndis-miniport_co_create_vc.md">MiniportCoCreateVc</a> function that the
    driver calls in the context of setting up connections for outgoing and incoming calls.

Only connection-oriented miniport drivers that provide integrated call-management support can call 
    <b>NdisMCmCreateVc</b>. Stand-alone call managers and clients, which register themselves with NDIS as
    protocol drivers, call 
    <b>NdisCoCreateVc</b> instead.

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
<a href="..\ndis\nc-ndis-miniport_co_create_vc.md">MiniportCoCreateVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisallocatefromnpagedlookasidelist.md">
   NdisAllocateFromNPagedLookasideList</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisclmakecall.md">NdisClMakeCall</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndiscocreatevc.md">NdisCoCreateVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismcmdeletevc.md">NdisMCmDeleteVc</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismcmdispatchincomingcall.md">NdisMCmDispatchIncomingCall</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_cm_reg_sap.md">ProtocolCmRegisterSap</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_co_create_vc.md">ProtocolCoCreateVc</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisMCmCreateVc function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>