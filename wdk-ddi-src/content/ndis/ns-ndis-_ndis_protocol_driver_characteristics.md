---
UID : NS:ndis._NDIS_PROTOCOL_DRIVER_CHARACTERISTICS
title : _NDIS_PROTOCOL_DRIVER_CHARACTERISTICS
author : windows-driver-content
description : To specify its driver characteristics, a protocol driver initializes an NDIS_PROTOCOL_DRIVER_CHARACTERISTICS structure and passes it to NDIS.
old-location : netvista\ndis_protocol_driver_characteristics.htm
old-project : netvista
ms.assetid : db64c160-9db6-4b23-af14-e64acdb9ef57
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_PROTOCOL_DRIVER_CHARACTERISTICS, *PNDIS_PROTOCOL_DRIVER_CHARACTERISTICS, NDIS_PROTOCOL_DRIVER_CHARACTERISTICS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Windows
req.target-min-winverclnt : Supported in NDIS 6.0 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDIS_PROTOCOL_DRIVER_CHARACTERISTICS
req.alt-loc : ndis.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : See Remarks section
req.typenames : "*PNDIS_PROTOCOL_DRIVER_CHARACTERISTICS, NDIS_PROTOCOL_DRIVER_CHARACTERISTICS"
---

# _NDIS_PROTOCOL_DRIVER_CHARACTERISTICS structure
To specify its driver characteristics, a protocol driver initializes an
  <b>NDIS_PROTOCOL_DRIVER_CHARACTERISTICS</b> structure and passes it to NDIS.

## Syntax
````
typedef struct _NDIS_PROTOCOL_DRIVER_CHARACTERISTICS {
  NDIS_OBJECT_HEADER                     Header;
  UCHAR                                  MajorNdisVersion;
  UCHAR                                  MinorNdisVersion;
  UCHAR                                  MajorDriverVersion;
  UCHAR                                  MinorDriverVersion;
  ULONG                                  Flags;
  NDIS_STRING                            Name;
  SET_OPTIONS_HANDLER                    SetOptionsHandler;
  BIND_HANDLER_EX                        BindAdapterHandlerEx;
  UNBIND_HANDLER_EX                      UnbindAdapterHandlerEx;
  OPEN_ADAPTER_COMPLETE_HANDLER_EX       OpenAdapterCompleteHandlerEx;
  CLOSE_ADAPTER_COMPLETE_HANDLER_EX      CloseAdapterCompleteHandlerEx;
  NET_PNP_EVENT_HANDLER                  NetPnPEventHandler;
  UNINSTALL_PROTOCOL_HANDLER             UninstallHandler;
  OID_REQUEST_COMPLETE_HANDLER           OidRequestCompleteHandler;
  STATUS_HANDLER_EX                      StatusHandlerEx;
  RECEIVE_NET_BUFFER_LISTS_HANDLER       ReceiveNetBufferListsHandler;
  SEND_NET_BUFFER_LISTS_COMPLETE_HANDLER SendNetBufferListsCompleteHandler;
#if (NDIS_SUPPORT_NDIS61)
  DIRECT_OID_REQUEST_COMPLETE_HANDLER    DirectOidRequestCompleteHandler;
#endif 
} NDIS_PROTOCOL_DRIVER_CHARACTERISTICS, *PNDIS_PROTOCOL_DRIVER_CHARACTERISTICS;
````

## Members

        
            `BindAdapterHandlerEx`

            The entry point for the 
     <a href="..\ndis\nc-ndis-protocol_bind_adapter_ex.md">
     ProtocolBindAdapterEx</a> function.
        
            `CloseAdapterCompleteHandlerEx`

            The entry point for the 
     <a href="..\ndis\nc-ndis-protocol_close_adapter_complete_ex.md">
     ProtocolCloseAdapterCompleteEx</a> function.
        
            `DirectOidRequestCompleteHandler`

            The entry point of the caller's 
      <a href="..\ndis\nc-ndis-protocol_direct_oid_request_complete.md">
      ProtocolDirectOidRequestComplete</a> function. This is an optional function. Set this entry point to
      <b>NULL</b> if the protocol driver does not support the direct OID request interface.
        
            `Flags`

            Reserved for NDIS. Protocol drivers should set this member to zero.
        
            `Header`

            The 
     <a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a> structure for the
     <b>NDIS_PROTOCOL_DRIVER_CHARACTERISTICS</b> structure. Set the 
     <b>Type</b> member of the structure that 
     <b>Header</b> specifies to NDIS_OBJECT_TYPE_PROTOCOL_DRIVER_CHARACTERISTICS.
     

To indicate the version of the <b>NDIS_PROTOCOL_DRIVER_CHARACTERISTICS</b> structure, set the 
     <b>Revision</b> member to one of the following values:
        
            `MajorDriverVersion`

            Reserved for the major version number of the protocol driver. Protocol drivers can specify any
     value that they require.
        
            `MajorNdisVersion`

            The major version of the NDIS library the protocol driver is using. The current value is
     0x06.
        
            `MinorDriverVersion`

            Reserved for the minor version number of the protocol driver. Protocol drivers can specify any
     value that they require.
        
            `MinorNdisVersion`

            The minor NDIS version. The following are the available minor version value settings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
        
            `Name`

            A Unicode string that is the service name of the protocol driver.
        
            `NetPnPEventHandler`

            The entry point of the caller's 
     <a href="..\ndis\nc-ndis-protocol_net_pnp_event.md">ProtocolNetPnPEvent</a> function.
        
            `OidRequestCompleteHandler`

            The entry point of the caller's 
     <a href="..\ndis\nc-ndis-protocol_oid_request_complete.md">
     ProtocolOidRequestComplete</a> function.
        
            `OpenAdapterCompleteHandlerEx`

            The entry point for the 
     <a href="..\ndis\nc-ndis-protocol_open_adapter_complete_ex.md">
     ProtocolOpenAdapterCompleteEx</a> function.
        
            `ReceiveNetBufferListsHandler`

            The entry point for the 
     <a href="..\ndis\nc-ndis-protocol_receive_net_buffer_lists.md">
     ProtocolReceiveNetBufferLists</a> function.
        
            `SendNetBufferListsCompleteHandler`

            The entry point for the 
     <a href="..\ndis\nc-ndis-protocol_send_net_buffer_lists_complete.md">
     ProtocolSendNetBufferListsComplete</a> function.
        
            `SetOptionsHandler`

            The entry point for the 
     <a href="..\ndis\nc-ndis-set_options.md">ProtocolSetOptions</a> function.
        
            `StatusHandlerEx`

            The entry point of the caller's 
     <a href="..\ndis\nc-ndis-protocol_status_ex.md">ProtocolStatusEx</a> function, if any, or
     <b>NULL</b>.
        
            `UnbindAdapterHandlerEx`

            The entry point for the 
     <a href="..\ndis\nc-ndis-protocol_unbind_adapter_ex.md">
     ProtocolUnbindAdapterEx</a> function.
        
            `UninstallHandler`

            The entry point of the caller's 
     <a href="..\ndis\nc-ndis-protocol_uninstall.md">ProtocolUninstall</a> function, if any,
     or <b>NULL</b>.

    ## Remarks
        A protocol driver calls the 
    <a href="..\ndis\nf-ndis-ndisregisterprotocoldriver.md">
    NdisRegisterProtocolDriver</a> function to register its characteristics, including the default entry
    points for its protocol driver functions (<i>ProtocolXxx</i>). The protocol driver initializes an <b>NDIS_PROTOCOL_DRIVER_CHARACTERISTICS</b> structure
    and passes a pointer to this structure in the 
    <i>ProtocolCharacteristics</i> parameter of 
    <b>NdisRegisterProtocolDriver</b>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ndis\nf-ndis-ndisregisterprotocoldriver.md">NdisRegisterProtocolDriver</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_bind_adapter_ex.md">ProtocolBindAdapterEx</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_close_adapter_complete_ex.md">
   ProtocolCloseAdapterCompleteEx</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_direct_oid_request_complete.md">
   ProtocolDirectOidRequestComplete</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_net_pnp_event.md">ProtocolNetPnPEvent</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_oid_request_complete.md">ProtocolOidRequestComplete</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_open_adapter_complete_ex.md">
   ProtocolOpenAdapterCompleteEx</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_receive_net_buffer_lists.md">
   ProtocolReceiveNetBufferLists</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_send_net_buffer_lists_complete.md">
   ProtocolSendNetBufferListsComplete</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-set_options.md">ProtocolSetOptions</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_status_ex.md">ProtocolStatusEx</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_unbind_adapter_ex.md">ProtocolUnbindAdapterEx</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-protocol_uninstall.md">ProtocolUninstall</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_PROTOCOL_DRIVER_CHARACTERISTICS structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>