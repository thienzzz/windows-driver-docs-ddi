---
UID : NS:windot11._DOT11_WFD_DEVICE_CAPABILITY_CONFIG
title : _DOT11_WFD_DEVICE_CAPABILITY_CONFIG
author : windows-driver-content
description : The device capability configuration structure sent with an OID_DOT11_WFD_DEVICE_CAPABILITY request.
old-location : netvista\_dot11_wfd_device_capability_config.htm
old-project : netvista
ms.assetid : 918307D4-0952-4FF0-8591-522C7E92194A
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _DOT11_WFD_DEVICE_CAPABILITY_CONFIG, DOT11_WFD_DEVICE_CAPABILITY_CONFIG, *PDOT11_WFD_DEVICE_CAPABILITY_CONFIG
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : windot11.h
req.include-header : Windot11.h
req.target-type : Windows
req.target-min-winverclnt : Versions: Supported in Windows 8
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DOT11_WFD_DEVICE_CAPABILITY_CONFIG
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
req.typenames : DOT11_WFD_DEVICE_CAPABILITY_CONFIG, *PDOT11_WFD_DEVICE_CAPABILITY_CONFIG
req.product : Windows 10 or later.
---

# _DOT11_WFD_DEVICE_CAPABILITY_CONFIG structure


## Syntax
````
typedef struct _DOT11_WFD_DEVICE_CAPABILITY_CONFIG {
  NDIS_OBJECT_HEADER Header;
  BOOLEAN            bServiceDiscoveryEnabled;
  BOOLEAN            bClientDiscoverabilityEnabled;
  BOOLEAN            bConcurrentOperationSupported;
  BOOLEAN            bInfrastructureManagementEnabled;
  BOOLEAN            bDeviceLimitReached;
  BOOLEAN            bInvitationProcedureEnabled;
  ULONG              WPSVersionsEnabled;
} DOT11_WFD_DEVICE_CAPABILITY_CONFIG, *PDOT11_WFD_DEVICE_CAPABILITY_CONFIG;
````

## Members

        
            `bClientDiscoverabilityEnabled`

            When set to TRUE, the miniport must enable Client Discoverability support. The miniport must also set the Client Discoverability bit in the P2P Device Capability Bitmap. If <b>bClientDiscoveryEnabled</b> is FALSE,  Client Discoverability support must be disabled and the miniport must ignore all Client Discovery packets it receives.

The system will set this to TRUE only if the miniport also sets TRUE for the <b>bClientDiscoverabilitySupported</b> member of <a href="..\windot11\ns-windot11-_dot11_wfd_attributes.md">DOT11_WFD_ATTRIBUTES</a>. The default value for this member is FALSE.
        
            `bConcurrentOperationSupported`

            When set to TRUE, the miniport must set the Concurrent Operation bit in the P2P Device Capability Bitmask. Otherwise, the Concurrent Operation bit must be cleared. The default value for this member is TRUE.
        
            `bDeviceLimitReached`

            When set to TRUE, the miniport must set the Device Limit bit of the P2P Device Capability Bitmask. Otherwise, this bit must be cleared. The default value for this member is FALSE.
        
            `bInfrastructureManagementEnabled`

            When set to TRUE, the miniport must enable P2P Managed Device support. The miniport must also set the P2P Infrastructure Managed bit in the P2P Device Capability Bitmap. Otherwise, the P2P Managed Device support must be disabled.

The system will set this member to TRUE only if the miniport also sets TRUE for the  <b>bInfrastructureManagementSupported</b> member of <a href="..\windot11\ns-windot11-_dot11_wfd_attributes.md">DOT11_WFD_ATTRIBUTES</a>. The default value for this member is FALSE
        
            `bInvitationProcedureEnabled`

            When set to TRUE, the miniport must set the P2P Invitation Procedure bit of the P2P Device Capability Bitmask. Otherwise, this bit must be cleared and the miniport must ignore all Invitation request/response packets it receives. The default value for this member is TRUE.
        
            `bServiceDiscoveryEnabled`

            When set to TRUE, the miniport must enable Service Discovery support. The miniport must also set the Service Discovery bit in the P2P Device Capability Bitmap. If <b>bServiceDiscoveryEnabled</b> is FALSE, Service Discovery support must be disabled and the miniport must ignore all Service Discovery packets it receives.

 The system will set this to TRUE only if the miniport also sets TRUE for the <b>bServiceDiscoverySupported</b> member of <a href="..\windot11\ns-windot11-_dot11_wfd_attributes.md">DOT11_WFD_ATTRIBUTES</a>. The default value for this member is FALSE.
        
            `Header`

            Specifies the type, revision and size of the <b>DOT11_WFD_DEVICE_CAPABILITY_CONFIG</b> structure. The required settings for the members of <b>Header</b> are the following:

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
<td>DOT11_WFD_DEVICE_CAPABILITY_CONFIG_REVISION_1</td>
</tr>
<tr>
<td><b>Size</b></td>
<td>DOT11_SIZEOF_WFD_DEVICE_CAPABILITY_CONFIG_1</td>
</tr>
</table>
        
            `WPSVersionsEnabled`

            The versions of WPS enabled for the Wi-Fi Direct Device


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | windot11.h (include Windot11.h) |