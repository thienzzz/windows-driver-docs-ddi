---
UID : NS:ndis._NDIS_SWITCH_NIC_STATUS_INDICATION
title : _NDIS_SWITCH_NIC_STATUS_INDICATION
author : windows-driver-content
description : The NDIS_SWITCH_NIC_STATUS_INDICATION structure specifies the information that is required to forward or originate an NDIS status indication from an underlying physical network adapter.
old-location : netvista\ndis_switch_nic_status_indication.htm
old-project : netvista
ms.assetid : a3841a14-0876-47f4-a4dc-6231b76086ca
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_SWITCH_NIC_STATUS_INDICATION, NDIS_SWITCH_NIC_STATUS_INDICATION, *PNDIS_SWITCH_NIC_STATUS_INDICATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Windows
req.target-min-winverclnt : Supported in NDIS 6.30 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDIS_SWITCH_NIC_STATUS_INDICATION
req.alt-loc : Ndis.h
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
req.typenames : NDIS_SWITCH_NIC_STATUS_INDICATION, *PNDIS_SWITCH_NIC_STATUS_INDICATION
---

# _NDIS_SWITCH_NIC_STATUS_INDICATION structure
The <b>NDIS_SWITCH_NIC_STATUS_INDICATION</b> structure specifies the information that is required to forward or originate an NDIS status indication from an underlying physical network adapter.

## Syntax
````
typedef struct _NDIS_SWITCH_NIC_STATUS_INDICATION {
  NDIS_OBJECT_HEADER      Header;
  ULONG                   Flags;
  NDIS_SWITCH_PORT_ID     SourcePortId;
  NDIS_SWITCH_NIC_INDEX   SourceNicIndex;
  NDIS_SWITCH_PORT_ID     DestinationPortId;
  NDIS_SWITCH_NIC_INDEX   DestinationNicIndex;
  PNDIS_STATUS_INDICATION *StatusIndication;
} NDIS_SWITCH_NIC_STATUS_INDICATION, *PNDIS_SWITCH_NIC_STATUS_INDICATION;
````

## Members

        
            `DestinationNicIndex`

            An NDIS_SWITCH_NIC_INDEX value that specifies the index of the destination network adapter that is connected to the  extensible switch port specified by the <b>DestinationPortId</b> member.
        
            `DestinationPortId`

            An NDIS_SWITCH_PORT_ID value that contains the unique identifier of the extensible switch port to which the NDIS status indication is to be forwarded.
        
            `Flags`

            A ULONG value that contains a bitwise <b>OR</b> of flags. This member is reserved for NDIS.
        
            `Header`

            The type, revision, and size of the <b>NDIS_SWITCH_NIC_STATUS_INDICATION</b> structure. This member is formatted as an <a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a> structure.

The <b>Type</b> member of <b>Header</b> must be set to NDIS_OBJECT_TYPE_DEFAULT. To specify the version of the <b>NDIS_SWITCH_NIC_STATUS_INDICATION</b> structure, the <b>Revision</b> member of <b>Header</b> must be set to the following value:
        
            `SourceNicIndex`

            An NDIS_SWITCH_NIC_INDEX value that specifies the index of the source network adapter that is connected to the source extensible switch port. This port is specified by the <b>SourcePortId</b> member.
        
            `SourcePortId`

            An NDIS_SWITCH_PORT_ID value that contains the unique identifier of the Hyper-V extensible switch port from which the NDIS status indication was originally generated.
        
            `StatusIndication`

            A pointer to an <a href="..\ndis\ns-ndis-_ndis_status_indication.md">NDIS_STATUS_INDICATION</a> structure. This structure contains the data for the NDIS status indication originally issued by the source network adapter as specified by the <b>SourcePortId</b> and <b>SourceNicIndex</b> members.

    ## Remarks
        The <b>NDIS_SWITCH_NIC_STATUS_INDICATION</b> structure is used in NDIS status indications of <a href="https://msdn.microsoft.com/library/windows/hardware/hh598205">NDIS_STATUS_SWITCH_NIC_STATUS</a>.

An extension can forward or originate status indications from any underlying physical adapter that is connected to the extensible switch <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/external-network-adapters">external network adapter</a>. Typically, the extension issues these status indications in order to change the advertised hardware offload capabilities of the underlying physical adapter. 

The extension can forward or originate status notifications for the following types of hardware offloads:

Internet Protocol security (IPsec).

Virtualized machine queue (VMQ).

Single root I/O virtualization (SR-IOV).

For guidelines on how to issue NDIS status indications from underlying physical adapters, see <a href="https://msdn.microsoft.com/ECA336FD-3E07-47D8-9006-6FE9CC1BEC2F">Managing NDIS Status Indications from Physical Network Adapters</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |

    ## See Also

        <dl>
<dt><b></b></dt>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_ndis_status_indication.md">NDIS_STATUS_INDICATION</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_ndis_switch_nic_status_indication.md">NDIS_SWITCH_NIC_STATUS_INDICATION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_SWITCH_NIC_STATUS_INDICATION structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>