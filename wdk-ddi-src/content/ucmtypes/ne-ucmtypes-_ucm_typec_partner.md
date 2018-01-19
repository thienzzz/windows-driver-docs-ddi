---
UID : NE:ucmtypes._UCM_TYPEC_PARTNER
title : _UCM_TYPEC_PARTNER
author : windows-driver-content
description : Defines the state of the Type-C connector.
old-location : buses\ucm_type_c_port_state.htm
old-project : usbref
ms.assetid : 4779E943-5C13-4DE2-AF8F-37657F0F99C0
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _UCM_TYPEC_PARTNER, UCM_TYPEC_PARTNER
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ucmtypes.h
req.include-header : Ucmcx.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 1.15
req.umdf-ver : 2.15
req.alt-api : UCM_TYPEC_PARTNER
req.alt-loc : Ucmtypes.h
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
req.typenames : UCM_TYPEC_PARTNER
req.product : Windows 10 or later.
---

# _UCM_TYPEC_PARTNER Enumeration
Defines the state of the Type-C connector.

## Syntax
````
typedef enum _UCM_TYPEC_PARTNER { 
  UcmTypeCPartnerStateInvalid               = 0,
  UcmTypeCPartnerStateUfp ,
  UcmTypeCPartnerStateDfp ,
  UcmTypeCPartnerStatePoweredCableNoUfp ,
  UcmTypeCPartnerStatePoweredCableWithUfp ,
  UcmTypeCPartnerStateAudioAccessory,
  UcmTypeCPartnerStateDebugAccessory
} UCM_TYPEC_PARTNER;
````

## Constants

<table>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** | 1.15 |
| **Minimum UMDF version** | 2.15 |
| **Header** | ucmtypes.h (include Ucmcx.h) |

## See Also

<dl>
<dt>
<a href="..\ucmmanager\ns-ucmmanager-_ucm_connector_typec_attach_params.md">UCM_CONNECTOR_TYPEC_ATTACH_PARAMS</a>
</dt>
<dt>
<a href="..\ucmmanager\nf-ucmmanager-ucmconnectortypecattach.md">UcmConnectorTypeCAttach</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UCM_TYPEC_PARTNER enumeration%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>