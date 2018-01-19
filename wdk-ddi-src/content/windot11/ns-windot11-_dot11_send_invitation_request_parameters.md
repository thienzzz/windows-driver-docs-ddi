---
UID : NS:windot11._DOT11_SEND_INVITATION_REQUEST_PARAMETERS
title : _DOT11_SEND_INVITATION_REQUEST_PARAMETERS
author : windows-driver-content
description : The request parameters for an inivitation request are specified in a DOT11_SEND_INVITATION_REQUEST_PARAMETERS structure. This structure is sent with an OID_DOT11_WFD_SEND_INVITATION_REQUEST request to the miniport.
old-location : netvista\dot11_send_invitation_request_parameters.htm
old-project : netvista
ms.assetid : A1177154-4674-425C-A83B-A4A8FCD1729C
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _DOT11_SEND_INVITATION_REQUEST_PARAMETERS, *PDOT11_SEND_INVITATION_REQUEST_PARAMETERS, DOT11_SEND_INVITATION_REQUEST_PARAMETERS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : windot11.h
req.include-header : Windot11.h
req.target-type : Windows
req.target-min-winverclnt : Supported starting with   Windows 8.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DOT11_SEND_INVITATION_REQUEST_PARAMETERS
req.alt-loc : Windot11.h
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
req.typenames : "*PDOT11_SEND_INVITATION_REQUEST_PARAMETERS, DOT11_SEND_INVITATION_REQUEST_PARAMETERS"
req.product : Windows 10 or later.
---

# _DOT11_SEND_INVITATION_REQUEST_PARAMETERS structure


## Syntax
````
typedef struct _DOT11_SEND_INVITATION_REQUEST_PARAMETERS {
  NDIS_OBJECT_HEADER              Header;
  DOT11_DIALOG_TOKEN              DialogToken;
  DOT11_MAC_ADDRESS               PeerDeviceAddress;
  ULONG                           uSendTimeout;
  DOT11_WFD_CONFIGURATION_TIMEOUT MinimumConfigTimeout;
  DOT11_WFD_INVITATION_FLAGS      InvitationFlags;
  DOT11_MAC_ADDRESS               GroupBSSID;
  BOOLEAN                         bUseGroupBSSID;
  DOT11_WFD_CHANNEL               OperatingChannel;
  BOOLEAN                         bUseSpecifiedOperatingChannel;
  DOT11_WFD_GROUP_ID              GroupID;
  BOOLEAN                         bLocalGO;
  ULONG                           uIEsOffset;
  ULONG                           uIEsLength;
} DOT11_SEND_INVITATION_REQUEST_PARAMETERS, *PDOT11_SEND_INVITATION_REQUEST_PARAMETERS;
````

## Members

        
            `bLocalGO`

            The device with the source address in the group owner.
        
            `bUseGroupBSSID`

            If TRUE, the BSSID in <b>GroupBSSID</b> is included in the invitation request. Otherwise, <b>GroupBSSID</b> is not valid.
        
            `bUseSpecifiedOperatingChannel`

            If TRUE, the operating channel specified in <b>OperatingChannel</b> is included in the invitation request. Otherwise, the miniport driver can choose its own operating channel.
        
            `DialogToken`

            The dialog token to send  in the invitation request packet.
        
            `GroupBSSID`

            The BSSID used by the P2P Group Owner for its P2P Group.
        
            `GroupID`

            The P2P group identifier.
        
            `Header`

            The type, revision, and size of the <b>DOT11_SEND_INVITATION_REQUEST_PARAMETERS</b> structure. The required settings for the members of <b>Header</b> are the following.

<table>
<tr>
<th>Member</th>
<th>Setting</th>
</tr>
<tr>
<td><b>Type</b></td>
<td>NDIS_OBJECT_TYPE_DEFAULT</td>
</tr>
<tr>
<td><b>Revision</b></td>
<td>DOT11_SEND_INVITATION_REQUEST_PARAMETERS_REVISION_1</td>
</tr>
<tr>
<td><b>Size</b></td>
<td>DOT11_SIZEOF_SEND_INVITATION_REQUEST_PARAMETERS_REVISION_1</td>
</tr>
</table>
        
            `InvitationFlags`

            The operation flags for the P2P invitation procedure.
        
            `MinimumConfigTimeout`

            The configuration time-out required by the system  to change its mode of operation to a Peer-to-Peer (P2P) Group Owner or a P2P Client. The miniport driver can set this with a larger value if necessary.
        
            `OperatingChannel`

            The channel information to include in the Operating Channel attribute of the invitation request.
        
            `PeerDeviceAddress`

            The destination address of the WFD device receiving the invitation request packet.
        
            `uIEsLength`

            The length, in bytes, of the array of IEs provided at <b>uIEsOffset</b>.
        
            `uIEsOffset`

            The offset, in bytes,  of the array of additional information elements (IEs) the Wi-Fi Direct (WFD) port must add to the invitation request packet. This offset is from the start of the buffer that contains this structure.
        
            `uSendTimeout`

            The maximum time, in milliseconds, allowed to send the invitation request. If the time-out expires before the miniport has successfully transmitted the invitation request, it should indicate the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439779">NDIS_STATUS_DOT11_WFD_INVITATION_REQUEST_SEND_COMPLETE</a> with a failure status.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | windot11.h (include Windot11.h) |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439779">NDIS_STATUS_DOT11_WFD_INVITATION_REQUEST_SEND_COMPLETE</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451806">OID_DOT11_WFD_SEND_INVITATION_REQUEST</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20DOT11_SEND_INVITATION_REQUEST_PARAMETERS structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>