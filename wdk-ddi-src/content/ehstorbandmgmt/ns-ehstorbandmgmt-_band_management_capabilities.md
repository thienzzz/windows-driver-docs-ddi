---
UID : NS:ehstorbandmgmt._BAND_MANAGEMENT_CAPABILITIES
title : _BAND_MANAGEMENT_CAPABILITIES
author : windows-driver-content
description : The BAND_MANAGEMENT_CAPABILITIES structure contains the security capabilities available for a storage device. This structure is returned in the system buffer by the IOCTL_EHSTOR_BANDMGMT_QUERY_CAPABILITIES request.
old-location : storage\band_management_capabilities.htm
old-project : storage
ms.assetid : 102C7CEC-B1DD-49F6-AB7F-0CE0A22EBE54
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _BAND_MANAGEMENT_CAPABILITIES, BAND_MANAGEMENT_CAPABILITIES, *PBAND_MANAGEMENT_CAPABILITIES
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ehstorbandmgmt.h
req.include-header : EhStorBandMgmt.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows 8
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : BAND_MANAGEMENT_CAPABILITIES
req.alt-loc : EhStorBandMgmt.h
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
req.typenames : BAND_MANAGEMENT_CAPABILITIES, *PBAND_MANAGEMENT_CAPABILITIES
---

# _BAND_MANAGEMENT_CAPABILITIES structure
The <b>BAND_MANAGEMENT_CAPABILITIES</b> structure contains the security capabilities available for a storage device. This structure is returned in the system buffer by the <a href="..\ehstorbandmgmt\ni-ehstorbandmgmt-ioctl_ehstor_bandmgmt_query_capabilities.md">IOCTL_EHSTOR_BANDMGMT_QUERY_CAPABILITIES</a> request.

## Syntax
````
typedef struct _BAND_MANAGEMENT_CAPABILITIES {
  ULONG     StructSize;
  ULONG     Capabilities;
  ULONGLONG KeyProtectionMechanism;
  ULONG     MinAuthKeyLength;
  ULONG     MaxAuthKeyLength;
  ULONG     MaxBandCount;
  ULONG     MaxSimultaneousReencryptionCount;
  ULONG     BandMetadataSize;
} BAND_MANAGEMENT_CAPABILITIES, *PBAND_MANAGEMENT_CAPABILITIES;
````

## Members

        
            `BandMetadataSize`

            The size, in bytes, of the per band metadata store.
        
            `Capabilities`

            Security capability flags for a storage device. This is a bitwise OR value of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
        
            `KeyProtectionMechanism`

            The mechanism used to protect the media keys. This member is set to one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
        
            `MaxAuthKeyLength`

            The maximum length, in bytes, of the  band authentication or erase keys accepted by the storage device.
        
            `MaxBandCount`

            The maximum number of simultaneous bands configured in the storage device. This includes the global band.
        
            `MaxSimultaneousReencryptionCount`

            The number of simultaneous band re-encryptions the hardware on the device supports. If this member is 0, hardware-driven band re-encryptions are not supported.
        
            `MinAuthKeyLength`

            The minimum length, in bytes, of the  band authentication or erase keys accepted by the storage device.
        
            `StructSize`

            The size of this structure in bytes. Set to <b>sizeof</b>(BAND_MANAGEMENT_CAPABILITIES).

    ## Remarks
        If <b>CAPS_ACTIVATED</b> is not set in <b>Capabilities</b>, security functionality can be activated with the <a href="..\ehstorbandmgmt\ni-ehstorbandmgmt-ioctl_ehstor_bandmgmt_activate.md">IOCTL_EHSTOR_BANDMGMT_ACTIVATE</a> request.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ehstorbandmgmt.h (include EhStorBandMgmt.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ehstorbandmgmt\ni-ehstorbandmgmt-ioctl_ehstor_bandmgmt_activate.md">IOCTL_EHSTOR_BANDMGMT_ACTIVATE</a>
</dt>
<dt>
<a href="..\ehstorbandmgmt\ni-ehstorbandmgmt-ioctl_ehstor_bandmgmt_query_capabilities.md">IOCTL_EHSTOR_BANDMGMT_QUERY_CAPABILITIES</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20BAND_MANAGEMENT_CAPABILITIES structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>