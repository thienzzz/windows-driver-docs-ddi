---
UID : NS:ndiswwan._NDIS_WWAN_SET_SIGNAL_INDICATION
title : _NDIS_WWAN_SET_SIGNAL_INDICATION
author : windows-driver-content
description : The NDIS_WWAN_SET_SIGNAL_INDICATION structure represents the signal indication of the MB device.
old-location : netvista\ndis_wwan_set_signal_indication.htm
old-project : netvista
ms.assetid : 6ef6fdd4-7d52-436a-96ee-ed83fab33e7b
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_WWAN_SET_SIGNAL_INDICATION, NDIS_WWAN_SET_SIGNAL_INDICATION, *PNDIS_WWAN_SET_SIGNAL_INDICATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ndiswwan.h
req.include-header : Ndiswwan.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows 7 and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDIS_WWAN_SET_SIGNAL_INDICATION
req.alt-loc : ndiswwan.h
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
req.typenames : NDIS_WWAN_SET_SIGNAL_INDICATION, *PNDIS_WWAN_SET_SIGNAL_INDICATION
---

# _NDIS_WWAN_SET_SIGNAL_INDICATION structure
The NDIS_WWAN_SET_SIGNAL_INDICATION structure represents the signal indication of the MB
  device.

## Syntax
````
typedef struct _NDIS_WWAN_SET_SIGNAL_INDICATION {
  NDIS_OBJECT_HEADER         Header;
  WWAN_SET_SIGNAL_INDICATION SignalIndication;
} NDIS_WWAN_SET_SIGNAL_INDICATION, *PNDIS_WWAN_SET_SIGNAL_INDICATION;
````

## Members

        
            `Header`

            The header with type, revision, and size information about the NDIS_WWAN_SET_SIGNAL_INDICATION
     structure. The MB Service sets the header with the values that are shown in the following table when it
     sends the data structure to the miniport driver for 
     <i>set</i> operations. Miniport drivers must set the header with the same values when they send the data
     structure to the MB service.
     

<table>
<tr>
<th>Header submember</th>
<th>Value</th>
</tr>
<tr>
<td>
Type

</td>
<td>
NDIS_OBJECT_TYPE_DEFAULT

</td>
</tr>
<tr>
<td>
Revision

</td>
<td>
NDIS_WWAN_SET_SIGNAL_INDICATION_REVISION_1

</td>
</tr>
<tr>
<td>
Size

</td>
<td>
sizeof(NDIS_WWAN_SET_SIGNAL_INDICATION)

</td>
</tr>
</table>
 

For more information about these members, see 
     <a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a>.
        
            `SignalIndication`

            A formatted 
     <a href="..\wwan\ns-wwan-_wwan_set_signal_indication.md">
     WWAN_SET_SIGNAL_INDICATION</a> object that represents the frequency of RSSI interval and RSSI
     threshold notifications.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndiswwan.h (include Ndiswwan.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_object_header.md">NDIS_OBJECT_HEADER</a>
</dt>
<dt>
<a href="..\wwan\ns-wwan-_wwan_set_signal_indication.md">WWAN_SET_SIGNAL_INDICATION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_WWAN_SET_SIGNAL_INDICATION structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>