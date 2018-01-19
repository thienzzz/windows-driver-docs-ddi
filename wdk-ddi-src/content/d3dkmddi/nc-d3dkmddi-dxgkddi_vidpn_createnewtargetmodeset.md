---
UID : NC:d3dkmddi.DXGKDDI_VIDPN_CREATENEWTARGETMODESET
title : DXGKDDI_VIDPN_CREATENEWTARGETMODESET
author : windows-driver-content
description : The pfnCreateNewTargetModeSet function creates a new target mode set object within a specified VidPN object.
old-location : display\dxgk_vidpn_interface_pfncreatenewtargetmodeset.htm
old-project : display
ms.assetid : c52935b4-306f-4200-80d9-0cfab6998450
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DD_MULTISAMPLEQUALITYLEVELSDATA, DD_MULTISAMPLEQUALITYLEVELSDATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : pfnCreateNewTargetModeSet
req.alt-loc : d3dkmddi.h
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
req.typenames : DD_MULTISAMPLEQUALITYLEVELSDATA
---


# DXGKDDI_VIDPN_CREATENEWTARGETMODESET callback function
The <b>pfnCreateNewTargetModeSet</b> function creates a new target mode set object within a specified VidPN object.

## Syntax

```
DXGKDDI_VIDPN_CREATENEWTARGETMODESET DxgkddiVidpnCreatenewtargetmodeset;

NTSTATUS DxgkddiVidpnCreatenewtargetmodeset(
  IN_CONST_D3DKMDT_HVIDPN hVidPn,
  IN_CONST_D3DDDI_VIDEO_PRESENT_TARGET_ID VidPnTargetId,
  OUT_PD3DKMDT_HVIDPNTARGETMODESET phNewVidPnTargetModeSet,
  DEREF_OUT_CONST_PPDXGK_VIDPNTARGETMODESET_INTERFACE ppVidPnTargetModeSetInterace
)
{...}
```

## Parameters

`hVidPn`

[in] A handle to a VidPN object. The VidPN manager previously provided this handle to the display miniport driver by calling <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_enumvidpncofuncmodality.md">DxgkDdiEnumVidPnCofuncModality</a>, <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_issupportedvidpn.md">DxgkDdiIsSupportedVidPn</a>, or <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_recommendfunctionalvidpn.md">DxgkDdiRecommendFunctionalVidPn</a>.

`VidPnTargetId`

[in] An integer that identifies one of the video present targets associated with the VidPN object.

`phNewVidPnTargetModeSet`

[out] A pointer to a variable that receives a handle to the newly created target mode set object.

`ppVidPnTargetModeSetInterace`

[out] A pointer to a variable that receives a pointer to a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_vidpntargetmodeset_interface.md">DXGK_VIDPNTARGETMODESET_INTERFACE</a> structure. The structure contains pointers to functions that the display miniport driver can call to inspect and alter the target mode set object.


## Return Value

The <b>pfnCreateNewTargetModeSet</b> function returns one of the following values:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The function succeeded.
<dl>
<dt><b>STATUS_GRAPHICS_INVALID_VIDPN</b></dt>
</dl>The handle supplied in <i>hVidPn</i> was invalid.
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>The VidPN manager was unable to allocate the memory required to create the new target mode set object.

## Remarks

To assign a new target mode set to a particular target in a VidPN implementation, perform the following steps:

Call <b>pfnCreateNewTargetModeSet</b> to get a handle to a new target mode set object. That target mode set object belongs to a particular VidPN object that you specify.

Use the functions of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_vidpntargetmodeset_interface.md">DXGK_VIDPNTARGETMODESET_INTERFACE</a> structure to add modes to the target mode set object.

Call <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpn_assigntargetmodeset.md">pfnAssignTargetModeSet</a> to assign the new target mode set to a particular target.

If you obtain a handle by calling <b>pfnCreateNewTargetModeSet</b> and then pass that handle to <b>pfnAssignTargetModeSet</b>, you do not need to release  the handle by calling <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpn_releasetargetmodeset.md">pfnReleaseTargetModeSet</a>.

If you obtain a handle by calling <b>pfnCreateNewTargetModeSet</b> and then you decide not to assign the new target mode set to a target, you must release the newly obtained handle by calling <b>pfnReleaseTargetModeSet</b>.

The lifetime of the DXGK_VIDPNTARGETEMODESET_INTERFACE structure returned in <i>ppVidPnTargetModeSetInterface</i> is owned by the operating system. Using this ownership scheme, the operating system can switch to newer implementations at run time without breaking clients of the interface.

The D3DKMDT_HVIDPN and D3DKMDT_HVIDPNTARGETMODESET data types are defined in <i>D3dkmdt.h</i>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570559">VidPN Target Mode Set Interface</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpn_assigntargetmodeset.md">pfnAssignTargetModeSet</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpn_releasetargetmodeset.md">pfnReleaseTargetModeSet</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGKDDI_VIDPN_CREATENEWTARGETMODESET callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>