---
UID : NS:fwpsk.FWPS_TRANSPORT_SEND_PARAMS1_
title : FWPS_TRANSPORT_SEND_PARAMS1_
author : windows-driver-content
description : The FWPS_TRANSPORT_SEND_PARAMS1 structure defines properties of an outbound transport layer packet.Note  FWPS_TRANSPORT_SEND_PARAMS1 is the specific version of FWPS_TRANSPORT_SEND_PARAMS used in Windows 7 and later.
old-location : netvista\fwps_transport_send_params1.htm
old-project : netvista
ms.assetid : 8d5653e4-a755-4066-b25a-f8f589821412
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FWPS_TRANSPORT_SEND_PARAMS1_, FWPS_TRANSPORT_SEND_PARAMS1
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows 7.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FWPS_TRANSPORT_SEND_PARAMS1
req.alt-loc : fwpsk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : FWPS_TRANSPORT_SEND_PARAMS1
---

# FWPS_TRANSPORT_SEND_PARAMS1_ structure
The <b>FWPS_TRANSPORT_SEND_PARAMS1</b> structure defines properties of an outbound transport layer
  packet.

## Syntax
````
typedef struct FWPS_TRANSPORT_SEND_PARAMS1_ {
  UCHAR      *remoteAddress;
  SCOPE_ID   remoteScopeId;
  WSACMSGHDR *controlData;
  ULONG      controlDataLength;
  UCHAR      *headerIncludeHeader;
  ULONG      headerIncludeHeaderLength;
} FWPS_TRANSPORT_SEND_PARAMS1;
````

## Members

        
            `remoteAddress`

            A pointer to a buffer that specifies the remote IP address to which the socket needs to be sent.
     The remote address specified by this member can be different than the one passed as one of the incoming
     data values to the callout driver's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function.
     

The buffer can contain an IPv4 address (4 bytes) or an IPv6 address (16 bytes), and the address must
     be specified in network byte order. The IP version must match the 
     <i>AddressFamily</i> parameter specified in the 
     <a href="..\fwpsk\nf-fwpsk-fwpsinjecttransportsendasync1.md">
     FwpsInjectTransportSendAsync1</a> function.

The buffer must remain valid until the injection completion function is called.
        
            `remoteScopeId`

            A <b>SCOPE_ID</b> structure that contains the scope identifier for the remote IP address. The scope
     identifier is provided to a callout through the 
     <b>remoteScopeId</b> member of the 
     <a href="..\fwpsk\ns-fwpsk-fwps_incoming_metadata_values0_.md">
     FWPS_INCOMING_METADATA_VALUES0</a> structure that is passed to the callout driver's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function. The <b>SCOPE_ID</b>
     structure is defined in 
     Ws2ipdef.h as follows.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct {
  union {
    struct {
      ULONG  Zone : 28;
      ULONG  Level : 4;
    };
    ULONG  Value;
  };
} SCOPE_ID, *PSCOPE_ID;</pre>
</td>
</tr>
</table></span></div>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544964">CMSGHDR</a>
</dt>
<dt>
<a href="..\fwpsk\ns-fwpsk-fwps_incoming_metadata_values0_.md">
   FWPS_INCOMING_METADATA_VALUES0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpsinjecttransportsendasync1.md">
   FwpsInjectTransportSendAsync1</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_TRANSPORT_SEND_PARAMS1 structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>