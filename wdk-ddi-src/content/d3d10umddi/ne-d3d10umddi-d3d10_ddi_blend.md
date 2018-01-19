---
UID : NE:d3d10umddi.D3D10_DDI_BLEND
title : D3D10_DDI_BLEND
author : windows-driver-content
description : The D3D10_DDI_BLEND enumeration type contains values that identify blend modes in a call to the driver's CreateBlendState function.
old-location : display\d3d10_ddi_blend.htm
old-project : display
ms.assetid : 719cd6b3-4f48-4b26-95fe-6f5faac56c06
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D10_DDI_BLEND, D3D10_DDI_BLEND
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D10_DDI_BLEND
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
req.typenames : D3D10_DDI_BLEND
---

# D3D10_DDI_BLEND Enumeration
The D3D10_DDI_BLEND enumeration type contains values that identify blend modes in a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createblendstate.md">CreateBlendState</a> function.

## Syntax
````
typedef enum D3D10_DDI_BLEND { 
  D3D10_DDI_BLEND_ZERO             = 1,
  D3D10_DDI_BLEND_ONE              = 2,
  D3D10_DDI_BLEND_SRC_COLOR        = 3,
  D3D10_DDI_BLEND_INV_SRC_COLOR    = 4,
  D3D10_DDI_BLEND_SRC_ALPHA        = 5,
  D3D10_DDI_BLEND_INV_SRC_ALPHA    = 6,
  D3D10_DDI_BLEND_DEST_ALPHA       = 7,
  D3D10_DDI_BLEND_INV_DEST_ALPHA   = 8,
  D3D10_DDI_BLEND_DEST_COLOR       = 9,
  D3D10_DDI_BLEND_INV_DEST_COLOR   = 10,
  D3D10_DDI_BLEND_SRC_ALPHASAT     = 11,
  D3D10_DDI_BLEND_BLEND_FACTOR     = 14,
  D3D10_DDI_BLEND_INVBLEND_FACTOR  = 15,
  D3D10_DDI_BLEND_SRC1_COLOR       = 16,
  D3D10_DDI_BLEND_INV_SRC1_COLOR   = 17,
  D3D10_DDI_BLEND_SRC1_ALPHA       = 18,
  D3D10_DDI_BLEND_INV_SRC1_ALPHA   = 19
} D3D10_DDI_BLEND;
````

## Constants

<table>

<tr>
<td>D3D10_DDI_BLEND_BLEND_FACTOR</td>
<td>Constant color-blending factor that the frame-buffer blender uses.</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_DEST_ALPHA</td>
<td>Blend factor is (A<sub>d</sub>, A<sub>d</sub>, A<sub>d</sub>, A<sub>d</sub>) of the current render target that is being blended.</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_DEST_COLOR</td>
<td>Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>) of the current render target that is being blended.</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INV_DEST_ALPHA</td>
<td>Blend factor is (1 - A<sub>d</sub>, 1 - A<sub>d</sub>, 1 - A<sub>d</sub>, 1 - A<sub>d</sub>) of the current render target that is being blended.</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INV_DEST_COLOR</td>
<td>Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>) of the current render target that is being blended.</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INV_SRC_ALPHA</td>
<td>Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INV_SRC_COLOR</td>
<td>Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INV_SRC1_ALPHA</td>
<td>Blend factor is the inversion of the alpha component of a pixel shader output register (1.0f - PS output o1.a).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INV_SRC1_COLOR</td>
<td>Blend factor is the inversion of the RGB components of a pixel shader output register (1.0f - PS output o1.rgb).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_INVBLEND_FACTOR</td>
<td>Inverted constant color-blending factor that the frame-buffer blender uses.</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_ONE</td>
<td>Blend factor is (1, 1, 1, 1).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_SRC_ALPHA</td>
<td>Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_SRC_ALPHASAT</td>
<td>Blend factor is (f, f, f, 1); f = min(A, 1 - A<sub>d</sub>).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_SRC_COLOR</td>
<td>Blend factor is (Rₛ,Gₛ,Bₛ,Aₛ).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_SRC1_ALPHA</td>
<td>Blend factor is the alpha component of a pixel shader output register (PS output o1.a).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_SRC1_COLOR</td>
<td>Blend factor is the red, green, and blue (RGB) components of a pixel shader output register (PS output o1.rgb).</td>
</tr>

<tr>
<td>D3D10_DDI_BLEND_ZERO</td>
<td>Blend factor is (0, 0, 0, 0).</td>
</tr>
</table>

## Remarks

A <i>blend mode</i> is an algorithm that is used to determine how a texture is blended with the colors of the surface that the texture is applied to. A <i>blend factor</i> is a description of how each color component is blended in texture blending.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |

## See Also

<dl>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createblendstate.md">CreateBlendState</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3D10_DDI_BLEND enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>