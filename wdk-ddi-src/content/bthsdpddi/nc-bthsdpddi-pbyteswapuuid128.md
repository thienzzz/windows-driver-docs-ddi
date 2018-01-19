---
UID : NC:bthsdpddi.PBYTESWAPUUID128
title : PBYTESWAPUUID128
author : windows-driver-content
description : The Bluetooth SdpByteSwapUuid128 function is used to reverse the byte order of a 128-bit universally unique identifier (UUID).
old-location : bltooth\sdpbyteswapuuid128.htm
old-project : bltooth
ms.assetid : 2598ebb3-1c9c-4ec1-b172-8c6d53415c9d
ms.author : windowsdriverdev
ms.date : 12/21/2017
ms.keywords : _BTH_VENDOR_SPECIFIC_COMMAND, *PBTH_VENDOR_SPECIFIC_COMMAND, BTH_VENDOR_SPECIFIC_COMMAND
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : bthsdpddi.h
req.include-header : BthSdpddi.h
req.target-type : Desktop
req.target-min-winverclnt : Versions: Supported in Windows Vista, and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : SdpByteSwapUuid128
req.alt-loc : sdplib.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= PASSIVE_LEVEL
req.typenames : "*PBTH_VENDOR_SPECIFIC_COMMAND, BTH_VENDOR_SPECIFIC_COMMAND"
---


# PBYTESWAPUUID128 callback function
The Bluetooth 
  <b>SdpByteSwapUuid128</b> function is used to reverse the byte order of a 128-bit universally unique
  identifier (UUID).

## Syntax

```
PBYTESWAPUUID128 Pbyteswapuuid128;

void Pbyteswapuuid128(
  GUID *pUuidFrom,
  GUID *pUuiidTo
)
{...}
```

## Parameters

`*pUuidFrom`



`*pUuiidTo`




## Return Value

None

## Remarks

The 
    <b>SdpByteSwapUuid128</b> function always reverses the byte order of the value pointed to by the *
    <i>pUuidFrom</i> parameter. Writers of Bluetooth device drivers can use this function to convert 128-bit
    GUID values from the byte order on the local computer to the byte order of the network that the computer
    is connected to.

Bluetooth profile drivers can obtain a pointer to this function through the 
    <a href="..\bthsdpddi\ns-bthsdpddi-_bthddi_sdp_parse_interface.md">BTHDDI_SDP_PARSE_INTERFACE</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | bthsdpddi.h (include BthSdpddi.h) |
| **Library** |  |
| **IRQL** | <= PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\bthsdpddi\ns-bthsdpddi-_bthddi_sdp_parse_interface.md">BTHDDI_SDP_PARSE_INTERFACE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [bltooth\bltooth]:%20PBYTESWAPUUID128 callback function%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>