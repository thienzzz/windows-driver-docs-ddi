---
UID : NC:d3d10umddi.PFND3D10_1DDI_CREATESHADERRESOURCEVIEW
title : PFND3D10_1DDI_CREATESHADERRESOURCEVIEW
author : windows-driver-content
description : The CreateShaderResourceView(D3D10_1) function creates a shader resource view.
old-location : display\createshaderresourceview_d3d10_1_.htm
old-project : display
ms.assetid : 7a0a92d2-a5df-4bee-a950-8a89aeb3dbb8
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _SETRESULT_INFO, *PSETRESULT_INFO, SETRESULT_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Desktop
req.target-min-winverclnt : CreateShaderResourceView(D3D10_1) is supported on Windows Vista with Service Pack 1 (SP1) and later versions and Windows Server 2008 and later versions.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : CreateShaderResourceView_d3d10_1_
req.alt-loc : d3d10umddi.h
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


# PFND3D10_1DDI_CREATESHADERRESOURCEVIEW callback function
The <b>CreateShaderResourceView(D3D10_1)</b> function creates a shader resource view.

## Syntax

```
PFND3D10_1DDI_CREATESHADERRESOURCEVIEW Pfnd3d101DdiCreateshaderresourceview;

void Pfnd3d101DdiCreateshaderresourceview(
   D3D10DDI_HDEVICE,
  CONST D3D10_1DDIARG_CREATESHADERRESOURCEVIEW *,
   D3D10DDI_HSHADERRESOURCEVIEW,
   D3D10DDI_HRTSHADERRESOURCEVIEW
)
{...}
```

## Parameters

`D3D10DDI_HDEVICE`



`*`



`D3D10DDI_HSHADERRESOURCEVIEW`



`D3D10DDI_HRTSHADERRESOURCEVIEW`




## Return Value

None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the Remarks section.

## Remarks

The driver might run out of memory. Therefore, the driver can pass E_OUTOFMEMORY or D3DDDIERR_DEVICEREMOVED in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function. The Direct3D runtime will determine that any other errors are critical. If the driver passes any errors, including D3DDDIERR_DEVICEREMOVED, the Direct3D runtime will determine that the handle is invalid; therefore, the runtime will not call the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroyshaderresourceview.md">DestroyShaderResourceView</a> function to destroy the handle that the <i>hShaderResourceView</i> parameter specifies.

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
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10_1ddi_calcprivateshaderresourceviewsize.md">CalcPrivateShaderResourceViewSize(D3D10_1)</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d10_1ddi_devicefuncs.md">D3D10_1DDI_DEVICEFUNCS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d10_1ddiarg_createshaderresourceview.md">D3D10_1DDIARG_CREATESHADERRESOURCEVIEW</a>
</dt>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_destroyshaderresourceview.md">DestroyShaderResourceView</a>
</dt>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D10_1DDI_CREATESHADERRESOURCEVIEW callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>