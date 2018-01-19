---
UID : NC:hdaudio.PGET_LINK_POSITION_REGISTER
title : PGET_LINK_POSITION_REGISTER
author : windows-driver-content
description : The GetLinkPositionRegister routine retrieves a pointer to a DMA engine's link position register.The function pointer type for a GetLinkPositionRegister routine is defined as:
old-location : audio\getlinkpositionregister.htm
old-project : audio
ms.assetid : 8b8c7f61-c22a-421f-999f-291999bb243f
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _SM_SetRNIDMgmtInfo_OUT, SM_SetRNIDMgmtInfo_OUT, *PSM_SetRNIDMgmtInfo_OUT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : hdaudio.h
req.include-header : Hdaudio.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : GetLinkPositionRegister
req.alt-loc : hdaudio.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <=DISPATCH_LEVEL
req.typenames : SM_SetRNIDMgmtInfo_OUT, *PSM_SetRNIDMgmtInfo_OUT
---


# PGET_LINK_POSITION_REGISTER callback function
The <code>GetLinkPositionRegister</code> routine retrieves a pointer to a DMA engine's link position register.

The function pointer type for a <code>GetLinkPositionRegister</code> routine is defined as:

## Syntax

```
PGET_LINK_POSITION_REGISTER PgetLinkPositionRegister;

NTSTATUS PgetLinkPositionRegister(
  PVOID _context,
  HANDLE Handle,
  PULONG *Position
)
{...}
```

## Parameters

`_context`



`Handle`



`*Position`




## Return Value

<code>GetLinkPositionRegister</code> returns STATUS_SUCCESS if the call succeeds. Otherwise, the routine returns an appropriate error code. The following table shows a possible return status code.
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>Indicates that the <i>handle</i> parameter value is invalid.

## Remarks

For more information, see <a href="https://msdn.microsoft.com/6764affc-a4f0-4568-aa27-7f12e86b818b">Wall Clock and Link Position Registers</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hdaudio.h (include Hdaudio.h) |
| **Library** |  |
| **IRQL** | <=DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\hdaudio\ns-hdaudio-_hdaudio_bus_interface.md">HDAUDIO_BUS_INTERFACE</a>
</dt>
<dt>
<a href="..\hdaudio\ns-hdaudio-_hdaudio_bus_interface_v2.md">HDAUDIO_BUS_INTERFACE_V2</a>
</dt>
<dt>
<a href="..\hdaudio\ns-hdaudio-_hdaudio_bus_interface_bdl.md">HDAUDIO_BUS_INTERFACE_BDL</a>
</dt>
<dt>
<a href="..\hdaudio\nc-hdaudio-pallocate_capture_dma_engine.md">AllocateCaptureDmaEngine</a>
</dt>
<dt>
<a href="..\hdaudio\nc-hdaudio-pallocate_render_dma_engine.md">AllocateRenderDmaEngine</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20PGET_LINK_POSITION_REGISTER callback function%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>