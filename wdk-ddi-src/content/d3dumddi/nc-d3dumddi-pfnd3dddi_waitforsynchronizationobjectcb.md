---
UID : NC:d3dumddi.PFND3DDDI_WAITFORSYNCHRONIZATIONOBJECTCB
title : PFND3DDDI_WAITFORSYNCHRONIZATIONOBJECTCB
author : windows-driver-content
description : The pfnWaitForSynchronizationObjectCb function inserts a wait for the specified synchronization objects in the specified context DMA stream.
old-location : display\pfnwaitforsynchronizationobjectcb.htm
old-project : display
ms.assetid : d33ca665-897d-4e99-b9a6-b794127fecfd
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_PTE, DXGK_PTE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnWaitForSynchronizationObjectCb
req.alt-loc : d3dumddi.h
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


# PFND3DDDI_WAITFORSYNCHRONIZATIONOBJECTCB callback function
The <b>pfnWaitForSynchronizationObjectCb</b> function inserts a wait for the specified synchronization objects in the specified context DMA stream.

## Syntax

```
PFND3DDDI_WAITFORSYNCHRONIZATIONOBJECTCB Pfnd3dddiWaitforsynchronizationobjectcb;

HRESULT Pfnd3dddiWaitforsynchronizationobjectcb(
  HANDLE hDevice,
  CONST D3DDDICB_WAITFORSYNCHRONIZATIONOBJECT *
)
{...}
```

## Parameters

`hDevice`

A handle to a display device (that is, the graphics context).

`*`




## Return Value

<b>pfnWaitForSynchronizationObjectCb</b> returns one of the following values:
<dl>
<dt><b>S_OK</b></dt>
</dl>The wait was successfully set up.
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>Parameters were validated and determined to be incorrect.

 

This function might also return other HRESULT values.

## Remarks

<b>Direct3D Version 11 Note:  </b>For more information about how the driver calls <b>pfnWaitForSynchronizationObjectCb</b>, see <a href="https://msdn.microsoft.com/014a5e44-f8c4-45c0-96e8-d82f37b8b28d">Changes from Direct3D 10</a>.



<b>Direct3D Version 11 Note:  </b>For more information about how the driver calls <b>pfnWaitForSynchronizationObjectCb</b>, see <a href="https://msdn.microsoft.com/014a5e44-f8c4-45c0-96e8-d82f37b8b28d">Changes from Direct3D 10</a>.

For a code example of how to use the <b>pfnWaitForSynchronizationObjectCb</b> function, see <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_signalsynchronizationobjectcb.md">pfnSignalSynchronizationObjectCb</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_d3dddicb_waitforsynchronizationobject.md">D3DDDICB_WAITFORSYNCHRONIZATIONOBJECT</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DDDI_WAITFORSYNCHRONIZATIONOBJECTCB callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>