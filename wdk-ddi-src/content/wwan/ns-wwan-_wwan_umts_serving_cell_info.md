---
UID : NS:wwan._WWAN_UMTS_SERVING_CELL_INFO
title : _WWAN_UMTS_SERVING_CELL_INFO
author : windows-driver-content
description : The WWAN_UMTS_SERVING_CELL_INFO structure represents information about the UMTS serving cell.
old-location : netvista\wwan_umts_serving_cell_info.htm
old-project : netvista
ms.assetid : 62257D65-DCB9-43C3-A862-DAB31C27EF0A
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WWAN_UMTS_SERVING_CELL_INFO, *PWWAN_UMTS_SERVING_CELL_INFO, WWAN_UMTS_SERVING_CELL_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : wwan.h
req.include-header : Wwan.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10, version 1709
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WWAN_UMTS_SERVING_CELL_INFO
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
req.typenames : "*PWWAN_UMTS_SERVING_CELL_INFO, WWAN_UMTS_SERVING_CELL_INFO"
req.product : Windows 10 or later.
---

# _WWAN_UMTS_SERVING_CELL_INFO structure
The <b>WWAN_UMTS_SERVING_CELL_INFO</b> structure represents information about the UMTS serving cell.

## Syntax
````
typedef struct _WWAN_UMTS_SERVING_CELL_INFO {
  ULONG ProviderIdOffset;
  ULONG ProviderIdSize;
  ULONG LocationAreaCode;
  ULONG CellId;
  ULONG FrequencyInfoUL;
  ULONG FrequencyInfoDL;
  ULONG FrequencyInfoNT;
  ULONG UARFCN;
  ULONG PrimaryScramblingCode;
  ULONG RSCP;
  ULONG ECNO;
  ULONG PathLoss;
  BYTE  Data[ANYSIZE_ARRAY];
} WWAN_UMTS_SERVING_CELL_INFO, *PWWAN_UMTS_SERVING_CELL_INFO;
````

## Members

        
            `CellId`

            The Cell ID (0-268435455). Use 0xFFFFFFFF when this information is not available.
        
            `ECNO`

            The signal to noise ratio of the serving cell; the ratio of the received energy per PN chip for the CPICH to the total received. The range is -50 to 0, in units of 1dBm. Use 1 when this information is not available.
        
            `FrequencyInfoDL`

            The Frequency Info Downlink (0-16383). Use 0xFFFFFFFF when this information is not available.
        
            `FrequencyInfoNT`

            The Frequency Info for TDD (0-16383). Use 0xFFFFFFFF when this information is not available.
        
            `FrequencyInfoUL`

            The Frequency Info Uplink (0-16383). Use 0xFFFFFFFF when this information is not available.
        
            `LocationAreaCode`

            The Location Area Code (0-65535). Use 0xFFFFFFFF when this information is not available.
        
            `PathLoss`

            The path loss of the serving cell (46-173). Use 0xFFFFFFFF when this information is not available.
        
            `PrimaryScramblingCode`

            The Primary Scrambling Code of the serving cell (0-511). Use 0xFFFFFFFF when this information is not available.
        
            `ProviderIdOffset`

            The offset in bytes, calculated from the beginning of this structure, to a numeric (0-9) string called <i>ProviderId</i> that represents the network provider identity. This string is a concatenation of a three-digit Mobile Country Code (MCC) and a two or three-digit Mobile Network Code (MNC). This member can be NULL when no <i>ProviderId</i> information is returned.
        
            `ProviderIdSize`

            The size, in bytes, used for <i>ProviderId</i>.
        
            `RSCP`

            The Received Signal Code Power of the serving cell. The range is -120 to -25, in units of 1dBm. Use 0xFFFFFFFF when this information is not available.
        
            `UARFCN`

            The UTRA Absolute Radio Frequency Channel Number for the serving cell (0-16383). Use 0xFFFFFFFF when this information is not available.


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
<a href="..\wwan\ns-wwan-_wwan_base_stations_info.md">WWAN_BASE_STATIONS_INFO</a>
</dt>
<dt>
<a href="..\wwan\ns-wwan-_wwan_umts_mrl.md">WWAN_UMTS_MRL</a>
</dt>
<dt>
<a href="..\wwan\ns-wwan-_wwan_umts_mrl_info.md">WWAN_UMTS_MRL_INFO</a>
</dt>
<dt>
<a href="https://docs.microsoft.com/windows-hardware/drivers/network/mb-base-stations-information-query-support">MB base stations information query support</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20WWAN_UMTS_SERVING_CELL_INFO structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>