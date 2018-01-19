---
UID : NC:d3dumddi.PFND3DDDI_CHECKCOUNTER
title : PFND3DDDI_CHECKCOUNTER
author : windows-driver-content
description : Called by the Microsoft Direct3D runtime to retrieve info that describes a counter. Must be implemented by Windows Display Driver Model (WDDM) 1.3 and later user-mode display drivers.
old-location : display\pfncheckcounter.htm
old-project : display
ms.assetid : 3A8B040D-7B48-4CDB-985B-906AE1762E22
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_PTE, DXGK_PTE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dumddi.h
req.include-header : D3d10umddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnCheckCounter
req.alt-loc : D3dumddi.h
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
req.typenames : DXGK_PTE
---


# PFND3DDDI_CHECKCOUNTER callback function
Called by the Microsoft Direct3D runtime to retrieve info that describes a counter. Must be implemented by Windows Display Driver Model (WDDM) 1.3 and later user-mode display drivers.

## Syntax

```
PFND3DDDI_CHECKCOUNTER Pfnd3dddiCheckcounter;

HRESULT Pfnd3dddiCheckcounter(
  HANDLE hDevice,
   D3DDDIQUERYTYPE,
  D3DDDI_COUNTER_TYPE *,
  UINT *,
   LPSTR,
  UINT *pNameLength,
   LPSTR,
  UINT *pUnitsLength,
   LPSTR,
  UINT *pDescriptionLength
)
{...}
```

## Parameters

`hDevice`

A handle to the display device (graphics context).

`D3DDDIQUERYTYPE`



`*`



`*`



`LPSTR`



`*pNameLength`



`LPSTR`



`*pUnitsLength`



`LPSTR`



`*pDescriptionLength`




## Return Value

If this routine succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code, including the following:
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>An out-of-range device-dependent counter is requested, or a string length is not large enough for a buffer to contain the entire string.

Even though all strings used in this function are based on Unicode, they are always in the English locale and are not localized to other locales.

## Remarks

This function should behave similarly to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_checkcounter.md">CheckCounter</a> function that supports Microsoft Direct3D 10 and later.

Counters are typically used by tools that capture a frame and play it back multiple times. The pass that records accurate timing info is separate from other  passes. In later passes, a different set of counters is used each time.
The priority should be to obtain an accurate correlation of counter results to draw calls, and the overhead incurred during playback can be sacrificed. The driver must insert flush calls or wait-for-idle calls to ensure an accurate correlation.

Typically an app can simultaneously monitor only a small number of possible native counters, which might number in the hundreds. Additionally, the driver must indicate the number of active counters used by monitoring each supported counter ID from the <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_createquery.md">D3DDDIQUERYTYPE</a> enumeration (both well-known counter IDs and device-specific counter IDs). For example, the driver can indicate that monitoring a <i>FillRateUtilized</i> variable requires 3 of the maximum 4 simultaneously active counters (indicated by the <i>pActiveCounters</i> parameter). The app can therefore also monitor another counter ID, as long as that counter ID requires one or fewer active counters.

If a counter ID can always be monitored (and it doesn't interfere with monitoring any other counter IDs), the number of simultaneous active counters required by the counter ID can be zero.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3d10umddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_checkcounter.md">CheckCounter</a>
</dt>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_createquery.md">D3DDDIQUERYTYPE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DDDI_CHECKCOUNTER callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>