---
UID : NF:ucmmanager.UcmConnectorPdSourceCaps
title : UcmConnectorPdSourceCaps function
author : windows-driver-content
description : Notifies the USB connector manager framework extension (UcmCx) with the power source capabilities of the connector.
old-location : buses\ucmconnectorpdsourcecaps.htm
old-project : usbref
ms.assetid : 7C52EE60-7903-42A7-B535-9B8ED7A4B021
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : UcmConnectorPdSourceCaps
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ucmmanager.h
req.include-header : Ucmcx.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 1.15
req.umdf-ver : 2.15
req.alt-api : UcmConnectorPdSourceCaps
req.alt-loc : UcmCxstub.lib,UcmCxstub.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : UcmCxstub.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : "*PPORT_DATA_1, PORT_DATA_1"
req.product : Windows 10 or later.
---


# UcmConnectorPdSourceCaps function
Notifies the USB connector manager framework extension (UcmCx) with the power source capabilities of the connector.

## Syntax

````
NTSTATUS UcmConnectorPdSourceCaps(
  [in] UCMCONNECTOR              Connector,
  [in] UCM_PD_POWER_DATA_OBJECT  Pdos[],
  [in] UCHAR                     PdoCount
);
````

## Parameters

`Connector`



`Pdos`



`PdoCount`




## Return Value

<b>UcmConnectorPdSourceCaps</b> returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method can return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> value.

## Remarks

If the connector (local connector) is the power source, the client driver can report the  capabilities and changes to those capabilities to UcmCx by using <b>UcmConnectorPdSourceCaps</b>. If connector is a the power sink, report the advertised capabilities received from partner by calling  <a href="..\ucmmanager\nf-ucmmanager-ucmconnectorpdpartnersourcecaps.md">UcmConnectorPdPartnerSourceCaps</a>. The client driver must call <b>UcmConnectorPdPartnerSourceCaps</b> each time the partner re-advertises its capabilities.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** | 1.15 |
| **Minimum UMDF version** | 2.15 |
| **Header** | ucmmanager.h (include Ucmcx.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ucmmanager\nf-ucmmanager-ucmconnectorcreate.md">UcmConnectorCreate</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UcmConnectorPdSourceCaps method%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>