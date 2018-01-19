---
UID : NC:d3d10umddi.PFND3D11_1DDI_CREATEVIDEOPROCESSORINPUTVIEW
title : PFND3D11_1DDI_CREATEVIDEOPROCESSORINPUTVIEW
author : windows-driver-content
description : Creates a resource view for a video processor. This view defines the input sample for the video processing operation.
old-location : display\createvideoprocessorinputview.htm
old-project : display
ms.assetid : f3942c53-e366-41c5-9f43-d093fa6b6ed6
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _SETRESULT_INFO, *PSETRESULT_INFO, SETRESULT_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : CreateVideoProcessorInputView
req.alt-loc : D3d10umddi.h
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
req.typenames : "*PSETRESULT_INFO, SETRESULT_INFO"
---


# PFND3D11_1DDI_CREATEVIDEOPROCESSORINPUTVIEW callback function
Creates a resource view for a video processor. This view defines the input sample for the video processing operation.

## Syntax

```
PFND3D11_1DDI_CREATEVIDEOPROCESSORINPUTVIEW Pfnd3d111DdiCreatevideoprocessorinputview;

HRESULT Pfnd3d111DdiCreatevideoprocessorinputview(
   D3D10DDI_HDEVICE,
  CONST D3D11_1DDIARG_CREATEVIDEOPROCESSORINPUTVIEW *,
   D3D11_1DDI_HVIDEOPROCESSORINPUTVIEW,
   D3D11_1DDI_HRTVIDEOPROCESSORINPUTVIEW
)
{...}
```

## Parameters

`D3D10DDI_HDEVICE`



`*`



`D3D11_1DDI_HVIDEOPROCESSORINPUTVIEW`



`D3D11_1DDI_HRTVIDEOPROCESSORINPUTVIEW`




## Return Value

<b>CreateVideoProcessorInputView</b> returns one of the following values:
<dl>
<dt><b>S_OK</b></dt>
</dl>The video processor input view was created successfully.
<dl>
<dt><b>D3DDDIERR_DEVICEREMOVED</b></dt>
</dl>The graphics adapter was removed.
<dl>
<dt><b>DXGI_ERROR_UNSUPPORTED</b></dt>
</dl>The D3D11_1DDIARG_CREATEVIDEOPROCESSORINPUTVIEW contained incorrect or unsupported data. For example, the driver should return <b>DXGI_ERROR_UNSUPPORTED</b> if the <b>FourCC</b> member specified an unsupported code value.
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
        Memory was not available to complete the operation.

## Remarks

The Direct3D runtime calls <i>CreateVideoProcessorInputView</i> after it has called the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_calcprivatevideoprocessorinputviewsize.md">CalcPrivateVideoProcessorInputViewSize</a>   to determine the size in bytes for the private data that the driver requires for the video processor input view. The runtime allocates the memory for this private data for the driver. The driver uses this memory to store private data that is related to the video processor input view.

When the runtime  calls <i>CreateVideoProcessorInputView</i>, it passes the handle to the private data memory in the <i>hView</i> parameter. This handle is actually a pointer to the memory.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_calcprivatevideoprocessorinputviewsize.md">CalcPrivateVideoProcessorInputViewSize</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddiarg_createvideoprocessorinputview.md">D3D11_1DDIARG_CREATEVIDEOPROCESSORINPUTVIEW</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D11_1DDI_CREATEVIDEOPROCESSORINPUTVIEW callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>