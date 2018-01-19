---
UID : NS:ntddndis._NDIS_NIC_SWITCH_CAPABILITIES
title : _NDIS_NIC_SWITCH_CAPABILITIES
author : windows-driver-content
description : The NDIS_NIC_SWITCH_CAPABILITIES structure specifies the capabilities of a NIC switch on the network adapter.
old-location : netvista\ndis_nic_switch_capabilities.htm
old-project : netvista
ms.assetid : bc4b56bd-583f-4b41-b5a7-90958ce65f42
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_NIC_SWITCH_CAPABILITIES, *PNDIS_NIC_SWITCH_CAPABILITIES, NDIS_NIC_SWITCH_CAPABILITIES
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddndis.h
req.include-header : Ndis.h
req.target-type : Windows
req.target-min-winverclnt : Supported in NDIS 6.20 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDIS_NIC_SWITCH_CAPABILITIES
req.alt-loc : Ntddndis.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : "*PNDIS_NIC_SWITCH_CAPABILITIES, NDIS_NIC_SWITCH_CAPABILITIES"
---

# _NDIS_NIC_SWITCH_CAPABILITIES structure
The <b>NDIS_NIC_SWITCH_CAPABILITIES</b> structure specifies the capabilities of a NIC switch on the network adapter.

## Syntax
````
typedef struct _NDIS_NIC_SWITCH_CAPABILITIES {
  NDIS_OBJECT_HEADER Header;
  ULONG              Flags;
  ULONG              NdisReserved1;
  ULONG              NumTotalMacAddresses;
  ULONG              NumMacAddressesPerPort;
  ULONG              NumVlansPerPort;
  ULONG              NdisReserved2;
  ULONG              NdisReserved3;
#if (NDIS_SUPPORT_NDIS630)
  ULONG              NicSwitchCapabilities;
  ULONG              MaxNumSwitches;
  ULONG              MaxNumVPorts;
  ULONG              NdisReserved4;
  ULONG              MaxNumVFs;
  ULONG              MaxNumQueuePairs;
  ULONG              NdisReserved5;
  ULONG              NdisReserved6;
  ULONG              NdisReserved7;
  ULONG              MaxNumQueuePairsPerNonDefaultVPort;
  ULONG              NdisReserved8;
  ULONG              NdisReserved9;
  ULONG              NdisReserved10;
  ULONG              NdisReserved11;
  ULONG              NdisReserved12;
  ULONG              MaxNumMacAddresses;
  ULONG              NdisReserved13;
  ULONG              NdisReserved14;
  ULONG              NdisReserved15;
  ULONG              NdisReserved16;
  ULONG              NdisReserved17;
#endif 
#if (NDIS_SUPPORT_NDIS660)
  ULONG              MaxNumRssCapableNonDefaultPFVPorts;
  ULONG              NumberOfIndirectionTableEntriesForDefaultVPort;
  ULONG              NumberOfIndirectionTableEntriesPerNonDefaultPFVPort;
  ULONG              MaxNumQueuePairsForDefaultVPort;
#endif 
} NDIS_NIC_SWITCH_CAPABILITIES, *PNDIS_NIC_SWITCH_CAPABILITIES;
````

## Members

        
            `Flags`

            A ULONG value that contains a bitwise OR of flags. This member is reserved for NDIS.
        
            `Header`

            The type, revision, and size of the <b>NDIS_NIC_SWITCH_CAPABILITIES</b> structure. This member is formatted as an <a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a> structure.

The miniport driver must set the <b>Type</b> member of <b>Header</b> to NDIS_OBJECT_TYPE_DEFAULT. To specify the version of the <b>NDIS_NIC_SWITCH_CAPABILITIES</b> structure, the driver must set the <b>Revision</b> member of <b>Header</b> to one of the following values:
        
            `MaxNumMacAddresses`

            A ULONG value that specifies the maximum number of unicast MAC address filters that are available on the NIC switch.  

<div class="alert"><b>Note</b>  This value must be greater than or equal to the value of <b>MaxNumVPorts</b>. This enables each VPort (including the default VPort) to be configured to have at least one unicast MAC address filter.</div>
<div> </div>
        
            `MaxNumQueuePairs`

            A ULONG value that specifies the maximum number of queue pairs that can be assigned to all VPorts. This includes the default VPort that is attached to the PF.

<div class="alert"><b>Note</b>  This value must be greater than or equal to the value of <b>MaxNumVPorts</b>.</div>
<div> </div>
        
            `MaxNumQueuePairsForDefaultVPort`

            A ULONG value that specifies the maximum number of queue pairs that can be assigned to the default VPort. 

This value is specified in powers of 2, and provides for asymmetric configuration and assignment of queue pairs to VPorts. For more information, see <a href="https://msdn.microsoft.com/B4BA1567-D536-4E7D-924C-7476FB82DAEB">Symmetric and Asymmetric Assignment of Queue Pairs</a>.
        
            `MaxNumQueuePairsPerNonDefaultVPort`

            A ULONG value that specifies the maximum number of queue pairs that can be assigned to a nondefault VPort. 

This value is specified in powers of 2, and provides for asymmetric configuration and assignment of queue pairs to VPorts. For more information, see <a href="https://msdn.microsoft.com/B4BA1567-D536-4E7D-924C-7476FB82DAEB">Symmetric and Asymmetric Assignment of Queue Pairs</a>.
        
            `MaxNumRssCapableNonDefaultPFVPorts`

            A ULONG value that specifies the maximum number of RSS-capable non-default PFVPorts.
        
            `MaxNumSwitches`

            A ULONG value that specifies the maximum number of switches that can be created on the network adapter's PCI Express (PCIe) Physical Function (PF).

<div class="alert"><b>Note</b>  Starting with Windows Server 2012, Windows only supports the default NIC switch on the network adapter. Therefore, this member must always be set to one. 
</div>
<div> </div>
        
            `MaxNumVFs`

            A ULONG value that specifies the maximum number of VFs that can be created on the NIC switch. 

<div class="alert"><b>Note</b>  Depending on the available hardware resources on the network adapter, the miniport driver can set the <b>MaxNumVFs</b> member to a value that is less than its <b>*NumVFs</b>
keyword. For more information about this keyword, see <a href="https://msdn.microsoft.com/5CA33B4F-E43A-4EB6-BCAB-365CA1FD3EF2">Standardized INF Keywords for SR-IOV</a>.</div>
<div> </div>
        
            `MaxNumVPorts`

            A ULONG value that specifies the maximum number of VPorts that can be created on a network adapter. This includes the default VPort that is always attached to the PF. 

<div class="alert"><b>Note</b>  The NIC switch must support at least (<b>MaxNumVFs</b> + 1) VPorts.</div>
<div> </div>
        
            `NdisReserved1`

            Reserved for NDIS.
        
            `NdisReserved10`

            Reserved for NDIS.
        
            `NdisReserved11`

            Reserved for NDIS.
        
            `NdisReserved12`

            Reserved for NDIS.
        
            `NdisReserved13`

            Reserved for NDIS.
        
            `NdisReserved14`

            Reserved for NDIS.
        
            `NdisReserved15`

            Reserved for NDIS.
        
            `NdisReserved16`

            Reserved for NDIS.
        
            `NdisReserved17`

            Reserved for NDIS.
        
            `NdisReserved2`

            Reserved for NDIS.
        
            `NdisReserved3`

            Reserved for NDIS.
        
            `NdisReserved4`

            Reserved for NDIS.
        
            `NdisReserved5`

            Reserved for NDIS.
        
            `NdisReserved6`

            Reserved for NDIS.
        
            `NdisReserved7`

            Reserved for NDIS.
        
            `NdisReserved8`

            Reserved for NDIS.
        
            `NdisReserved9`

            Reserved for NDIS.
        
            `NicSwitchCapabilities`

            A ULONG value that contains a bitwise OR of the following flags that specify the capabilities of the NIC switch:
        
            `NumberOfIndirectionTableEntriesForDefaultVPort`

            A ULONG value that specifies the number of indirection table entries for the default VPort.
        
            `NumberOfIndirectionTableEntriesPerNonDefaultPFVPort`

            A ULONG value that specifies the number of indirection table entries for each non-default PFVPort.
        
            `NumMacAddressesPerPort`

            A ULONG value that contains the number of MAC addresses that are supported for each port.

<div class="alert"><b>Note</b>  Drivers must set this member to zero for revision 2 and later revisions of this structure.</div>
<div> </div>
        
            `NumTotalMacAddresses`

            A ULONG value that contains the total number of media access control (MAC) addresses that the network adapter supports.

<div class="alert"><b>Note</b>  Drivers must set this member to zero for revision 2 and later revisions of this structure.</div>
<div> </div>
        
            `NumVlansPerPort`

            A ULONG value that contains the number of VLANs that are supported for each port.

<div class="alert"><b>Note</b>  Drivers must set this member to zero for revision 2 and later revisions of this structure.</div>
<div> </div>

    ## Remarks
        The <b>NDIS_NIC_SWITCH_CAPABILITIES</b> structure is used in the 
    members of the following structures:

The <b>HardwareNicSwitchCapabilities</b> and 
    <b>CurrentNicSwitchCapabilities</b> members of the 
    <a href="..\ndis\ns-ndis-_ndis_miniport_adapter_hardware_assist_attributes.md">
    NDIS_MINIPORT_ADAPTER_HARDWARE_ASSIST_ATTRIBUTES</a> structure.

The 
    <b>NicSwitchCapabilities</b> member of the 
    <a href="..\ndis\ns-ndis-_ndis_filter_attach_parameters.md">
    NDIS_FILTER_ATTACH_PARAMETERS</a> and 
    <a href="..\ndis\ns-ndis-_ndis_bind_parameters.md">NDIS_BIND_PARAMETERS</a> structures. 

OID query requests of <a href="netvista.oid_nic_switch_current_capabilities">
    OID_NIC_SWITCH_CURRENT_CAPABILITIES</a> and 
    <a href="netvista.oid_nic_switch_hardware_capabilities">
    OID_NIC_SWITCH_HARDWARE_CAPABILITIES</a> return an <b>NDIS_NIC_SWITCH_CAPABILITIES</b> structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddndis.h (include Ndis.h) |

    ## See Also

        <dl>
<dt><b></b></dt>
<dt>
<a href="..\ndis\ns-ndis-_ndis_bind_parameters.md">NDIS_BIND_PARAMETERS</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_ndis_filter_attach_parameters.md">NDIS_FILTER_ATTACH_PARAMETERS</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_ndis_miniport_adapter_hardware_assist_attributes.md">NDIS_MINIPORT_ADAPTER_HARDWARE_ASSIST_ATTRIBUTES</a>
</dt>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451816">OID_NIC_SWITCH_CREATE_VPORT</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569760">OID_NIC_SWITCH_CURRENT_CAPABILITIES</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569761">OID_NIC_SWITCH_HARDWARE_CAPABILITIES</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_NIC_SWITCH_CAPABILITIES structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>