---
UID : NE:windot11._DOT11_PHY_TYPE
title : _DOT11_PHY_TYPE
author : windows-driver-content
description : Important  The Native 802.11 Wireless LAN interface is deprecated in Windows 10 and later.
old-location : netvista\dot11_phy_type.htm
old-project : netvista
ms.assetid : 45ef8085-512e-4f9b-a7ea-e4f445555cf8
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _DOT11_PHY_TYPE, DOT11_PHY_TYPE, *PDOT11_PHY_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : windot11.h
req.include-header : Ndis.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DOT11_PHY_TYPE
req.alt-loc : windot11.h
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
req.typenames : DOT11_PHY_TYPE, *PDOT11_PHY_TYPE
req.product : Windows 10 or later.
---

# _DOT11_PHY_TYPE Enumeration


## Syntax
````
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = dot11_phy_type_unknown,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
````

## Constants

<table>

<tr>
<td>dot11_phy_type_any</td>
<td>Specifies an unknown or uninitialized PHY type.</td>
</tr>

<tr>
<td>dot11_phy_type_dsss</td>
<td>Specifies a direct sequence spread spectrum (DSSS) PHY.</td>
</tr>

<tr>
<td>dot11_phy_type_erp</td>
<td>Specifies an extended-rate 802.11g PHY (ERP).</td>
</tr>

<tr>
<td>dot11_phy_type_fhss</td>
<td>Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</td>
</tr>

<tr>
<td>dot11_phy_type_hrdsss</td>
<td>Specifies a high-rate DSSS (HRDSSS) 802.11b PHY.</td>
</tr>

<tr>
<td>dot11_phy_type_ht</td>
<td>Specifies a high-throughput (HT) 802.11n PHY. Each 802.11n PHY, whether dual-band or not, is
     specified as this PHY type.</td>
</tr>

<tr>
<td>dot11_phy_type_IHV_end</td>
<td>Specifies the end of the range that is used to define proprietary PHY types that are developed by
     an IHV.
     

The 
     <b>dot11_phy_type_IHV_end</b> enumerator value is valid only when the miniport driver is operating in
     ExtSTA mode.</td>
</tr>

<tr>
<td>dot11_phy_type_IHV_start</td>
<td>Specifies the start of the range that is used to define proprietary PHY types that are developed
     by an independent hardware vendor (IHV).
     

The 
     <b>dot11_phy_type_IHV_start</b> enumerator value is valid only when the miniport driver is operating in
     Extensible Station (ExtSTA) mode.</td>
</tr>

<tr>
<td>dot11_phy_type_irbaseband</td>
<td>Specifies an infrared (IR) baseband PHY.</td>
</tr>

<tr>
<td>dot11_phy_type_ofdm</td>
<td>Specifies an orthogonal frequency division multiplexing (OFDM) 802.11a PHY.</td>
</tr>

<tr>
<td>dot11_phy_type_unknown</td>
<td>Specifies an unknown or uninitialized PHY type.</td>
</tr>

<tr>
<td>dot11_phy_type_vht</td>
<td>Specifies a very high-throughput (VHT) 802.11ac PHY.</td>
</tr>
</table>

## Remarks

An IHV can assign a value for its proprietary PHY types from 
    <b>dot11_phy_type_IHV_start</b> through 
    <b>dot11_phy_type_IHV_end</b>. The IHV must assign a unique number from this range for each of its
    proprietary PHY types.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | windot11.h (include Ndis.h) |

## See Also

<dl>
<dt>
<a href="..\windot11\ns-windot11-dot11_association_completion_parameters.md">
   DOT11_ASSOCIATION_COMPLETION_PARAMETERS</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569407">OID_DOT11_RECV_SENSITIVITY_LIST</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569413">OID_DOT11_SCAN_REQUEST</a>
</dt>
<dt>
<a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/oid-dot11-supported-phy-types">OID_DOT11_SUPPORTED_PHY_TYPES</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20DOT11_PHY_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>