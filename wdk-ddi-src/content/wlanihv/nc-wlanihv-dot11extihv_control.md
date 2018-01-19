---
UID : NC:wlanihv.DOT11EXTIHV_CONTROL
title : DOT11EXTIHV_CONTROL
author : windows-driver-content
description : Important  The Native 802.11 Wireless LAN interface is deprecated in Windows 10 and later.
old-location : netvista\dot11extihvcontrol.htm
old-project : netvista
ms.assetid : 27e1f112-a961-4464-9048-b56394930453
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _DRIVER_INFO_8W, *LPDRIVER_INFO_8W, *PDRIVER_INFO_8W, DRIVER_INFO_8W, DRIVER_INFO_8
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : wlanihv.h
req.include-header : Wlanihv.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : Dot11ExtIhvControl
req.alt-loc : Wlanihv.h
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
req.typenames : "*LPDRIVER_INFO_8W, *PDRIVER_INFO_8W, DRIVER_INFO_8W"
req.product : Windows 10 or later.
---


# DOT11EXTIHV_CONTROL callback function


## Syntax

```
DOT11EXTIHV_CONTROL Dot11extihvControl;

DWORD Dot11extihvControl(
  HANDLE hIhvExtAdapter,
  DWORD dwInBufferSize,
  PBYTE pInBuffer,
  DWORD dwOutBufferSize,
  PBYTE pOutBuffer,
  PDWORD pdwBytesReturned
)
{...}
```

## Parameters

`hIhvExtAdapter`

The handle used by the IHV Extensions DLL to reference the WLAN adapter. This handle value was
     specified through a previous call to the 
     <a href="..\wlanihv\nc-wlanihv-dot11extihv_init_adapter.md">Dot11ExtIhvInitAdapter</a> IHV Handler function.

`dwInBufferSize`

The size, in bytes, of the input control buffer pointed to by the 
     <i>pInBuffer</i> parameter.

`pInBuffer`

A pointer to the input control buffer.

`dwOutBufferSize`

The size, in bytes, of the output buffer (if provided) pointed to by the 
     <i>pOutBuffer</i> parameter.

`pOutBuffer`

A pointer to the output buffer, if provided.

`pdwBytesReturned`

A pointer to a variable that contains the size, in bytes, of the response input/output
     buffer.


## Return Value

If the call succeeds, the function returns ERROR_SUCCESS. Otherwise, it returns an error code
     defined in 
     Winerror.h.

## Remarks

The operating system calls this function when the 
    <b>WlanIhvControl</b> function is called with the 
    <i>Type</i> parameter set to a value of 
    <b>wlan_ihv_control_type_service</b>. For a description of the 
    <b>WlanIhvControl</b> function, see the Microsoft Windows SDK documentation.

Data transferred with this function is not validated, so the IHV is responsible for correctly parsing
    the input buffer.

The data buffer pointed to by the 
    <i>pdwBytesReturned</i> parameter will always be returned. However, the buffer pointed to by 
    <i>pOutBuffer</i> will be copied only if a valid pointer is provided and the value pointed to by 
    <i>pdwBytesReturned</i> is less than or equal to 
    <i>dwOutBufferSize</i> .

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wlanihv.h (include Wlanihv.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wlanihv\nc-wlanihv-dot11extihv_init_adapter.md">Dot11ExtIhvInitAdapter</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20DOT11EXTIHV_CONTROL callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>