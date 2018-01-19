---
UID : NE:wwan._WWAN_PIN_TYPE
title : _WWAN_PIN_TYPE
author : windows-driver-content
description : The WWAN_PIN_TYPE enumeration lists the different types of Personal Identification Numbers (PINs) that are supported by the MB device.
old-location : netvista\wwan_pin_type.htm
old-project : netvista
ms.assetid : f6b8146e-dbe2-4c73-beb2-02868db9fb27
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WWAN_PIN_TYPE, *PWWAN_PIN_TYPE, WWAN_PIN_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wwan.h
req.include-header : Wwan.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows 7 and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WWAN_PIN_TYPE
req.alt-loc : wwan.h
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
req.typenames : "*PWWAN_PIN_TYPE, WWAN_PIN_TYPE"
req.product : Windows 10 or later.
---

# _WWAN_PIN_TYPE Enumeration
The WWAN_PIN_TYPE enumeration lists the different types of Personal Identification Numbers (PINs)
  that are supported by the MB device.

## Syntax
````
typedef enum _WWAN_PIN_TYPE { 
  WwanPinTypeNone               = 0,
  WwanPinTypeCustom,
  WwanPinTypePin1,
  WwanPinTypePin2,
  WwanPinTypeDeviceSimPin,
  WwanPinTypeDeviceFirstSimPin,
  WwanPinTypeNetworkPin,
  WwanPinTypeNetworkSubsetPin,
  WwanPinTypeSvcProviderPin,
  WwanPinTypeCorporatePin,
  WwanPinTypeSubsidyLock,
  WwanPinTypePuk1,
  WwanPinTypePuk2,
  WwanPinTypeDeviceFirstSimPuk,
  WwanPinTypeNetworkPuk,
  WwanPinTypeNetworkSubsetPuk,
  WwanPinTypeSvcProviderPuk,
  WwanPinTypeCorporatePuk,
  WwanPinTypeMax
} WWAN_PIN_TYPE, *PWWAN_PIN_TYPE;
````

## Constants

<table>

<tr>
<td>WwanPinTypeCorporatePin</td>
<td>The corporate personalization key.</td>
</tr>

<tr>
<td>WwanPinTypeCorporatePuk</td>
<td>The corporate personalization unlock key.</td>
</tr>

<tr>
<td>WwanPinTypeCustom</td>
<td>The PIN type is a custom type and is none of the other PIN types listed in this
     enumeration.</td>
</tr>

<tr>
<td>WwanPinTypeDeviceFirstSimPin</td>
<td>The device to very first SIM key.</td>
</tr>

<tr>
<td>WwanPinTypeDeviceFirstSimPuk</td>
<td>The device to very first SIM PIN unlock key.</td>
</tr>

<tr>
<td>WwanPinTypeDeviceSimPin</td>
<td>The device to SIM key.</td>
</tr>

<tr>
<td>WwanPinTypeMax</td>
<td>The total number of supported PIN types.</td>
</tr>

<tr>
<td>WwanPinTypeNetworkPin</td>
<td>The network personalization key.</td>
</tr>

<tr>
<td>WwanPinTypeNetworkPuk</td>
<td>The network personalization unlock key.</td>
</tr>

<tr>
<td>WwanPinTypeNetworkSubsetPin</td>
<td>The network subset personalization key.</td>
</tr>

<tr>
<td>WwanPinTypeNetworkSubsetPuk</td>
<td>The network subset personalization unlock key.</td>
</tr>

<tr>
<td>WwanPinTypeNone</td>
<td>No PIN is pending to be entered.</td>
</tr>

<tr>
<td>WwanPinTypePin1</td>
<td>The PIN1 key.</td>
</tr>

<tr>
<td>WwanPinTypePin2</td>
<td>The PIN2 key.</td>
</tr>

<tr>
<td>WwanPinTypePuk1</td>
<td>The Personal Identification Number1 Unlock Key (PUK1).</td>
</tr>

<tr>
<td>WwanPinTypePuk2</td>
<td>The Personal Identification Number2 Unlock Key (PUK2).</td>
</tr>

<tr>
<td>WwanPinTypeSubsidyLock</td>
<td>The subsidy unlock key.</td>
</tr>

<tr>
<td>WwanPinTypeSvcProviderPin</td>
<td>The service provider (SP) personalization key.</td>
</tr>

<tr>
<td>WwanPinTypeSvcProviderPuk</td>
<td>The service provider (SP) personalization unlock key.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wwan.h (include Wwan.h) |

## See Also

<dl>
<dt>
<a href="..\wwan\ns-wwan-_wwan_pin_info.md">WWAN_PIN_INFO</a>
</dt>
<dt>
<a href="..\wwan\ns-wwan-_wwan_pin_action.md">WWAN_PIN_ACTION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20WWAN_PIN_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>