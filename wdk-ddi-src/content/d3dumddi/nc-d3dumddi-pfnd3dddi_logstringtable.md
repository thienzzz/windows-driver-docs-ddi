---
UID : NC:d3dumddi.PFND3DDDI_LOGSTRINGTABLE
title : PFND3DDDI_LOGSTRINGTABLE
author : windows-driver-content
description : Called by the Microsoft Direct3D runtime to request that the user-mode display driver log a custom Event Tracing for Windows (ETW) marker event. Optionally implemented by Windows Display Driver Model (WDDM) 1.3 and later drivers.
old-location : display\logmarkerstringtable.htm
old-project : display
ms.assetid : DDB42924-5C28-4737-92C1-4FB7A00B09AA
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_PTE, DXGK_PTE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dumddi.h
req.include-header : D3d10umddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 8.1,WDDM 1.3 and later
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : LogMarkerStringTable
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


# PFND3DDDI_LOGSTRINGTABLE callback function
Called by the Microsoft Direct3D runtime to request that the user-mode display driver log a custom Event Tracing for Windows (ETW) marker event. Optionally implemented by Windows Display Driver Model (WDDM) 1.3 and later drivers.

## Syntax

```
PFND3DDDI_LOGSTRINGTABLE Pfnd3dddiLogstringtable;

HRESULT Pfnd3dddiLogstringtable(
  HANDLE hLog,
  PFND3DDDICB_LOGSTRINGTABLEENTRY pfnLogStringTableEntryCb
)
{...}
```

## Parameters

`hLog`

A handle to the Event Tracing for Windows (ETW) log that is to be written to.

`pfnLogStringTableEntryCb`

A function pointer to the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddicb_logstringtableentry.md">LogMarkerStringTableEntry</a> function that locates a string table entry.


## Return Value

Returns <b>S_OK</b> or an appropriate error result if the function does not complete successfully.

## Remarks

This function is free-threaded.

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
<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddicb_logstringtableentry.md">LogMarkerStringTableEntry</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DDDI_LOGSTRINGTABLE callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>