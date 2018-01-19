---
UID : NE:dxva._DXVA_VideoChromaSubsampling
title : _DXVA_VideoChromaSubsampling
author : windows-driver-content
description : The DXVA_VideoChromaSubsampling enumeration type contains enumerators that identify the chroma encoding scheme for Y'Cb'Cr' data.
old-location : display\dxva_videochromasubsampling.htm
old-project : display
ms.assetid : aa8f736f-1311-4217-8750-cdd134c6945c
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXVA_VideoChromaSubsampling, DXVA_VideoChromaSubsampling
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : dxva.h
req.include-header : Dxva.h
req.target-type : Windows
req.target-min-winverclnt : This enumeration type applies only to Windows Server 2003 with SP1 and later, and Windows XP with SP2 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXVA_VideoChromaSubsampling
req.alt-loc : dxva.h
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
req.typenames : DXVA_VideoChromaSubsampling
---

# _DXVA_VideoChromaSubsampling Enumeration
The DXVA_VideoChromaSubsampling enumeration type contains enumerators that identify the chroma encoding scheme for Y'Cb'Cr' data.

## Syntax
````
typedef enum _DXVA_VideoChromaSubsampling { 
  DXVA_VideoChromaSubsamplingShift                            = (DXVA_ExtColorData_ShiftBase + 0),
  DXVA_VideoChromaSubsamplingMask                             = DXVAColorMask(5, DXVA_VideoChromaSubsamplingShift),
  DXVA_VideoChromaSubsampling_Unknown                         = 0,
  DXVA_VideoChromaSubsampling_ProgressiveChroma               = 0x8,
  DXVA_VideoChromaSubsampling_Horizontally_Cosited            = 0x4,
  DXVA_VideoChromaSubsampling_Vertically_Cosited              = 0x2,
  DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes  = 0x1,
  DXVA_VideoChromaSubsampling_MPEG2                           = DXVA_VideoChromaSubsampling_Horizontally_Cosited | DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes,
  DXVA_VideoChromaSubsampling_MPEG1                           = DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes,
  DXVA_VideoChromaSubsampling_DV_PAL                          = DXVA_VideoChromaSubsampling_Horizontally_Cosited | DXVA_VideoChromaSubsampling_Vertically_Cosited,
  DXVA_VideoChromaSubsampling_Cosited                         = DXVA_VideoChromaSubsampling_Horizontally_Cosited | DXVA_VideoChromaSubsampling_Vertically_Cosited | DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes
} DXVA_VideoChromaSubsampling;
````

## Constants

<table>

<tr>
<td>DXVA_VideoChromaSubsampling_Cosited</td>
<td>A bitwise OR of the DXVA_VideoChromaSubsampling_Horizontally_Cosited, and DXVA_VideoChromaSubsampling_Vertically_Cosited, and DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes values that are used with 4:4:4, 4:2:2, and 4:1:1 data.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_DV_PAL</td>
<td>A bitwise OR of the DXVA_VideoChromaSubsampling_Horizontally_Cosited and DXVA_VideoChromaSubsampling_Vertically_Cosited values that are used with 4:2:0 data.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_Horizontally_Cosited</td>
<td>Specifies that chroma samples are aligned on multiples of the luma samples horizontally.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_MPEG1</td>
<td>The DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes value that is used with 4:2:0 data.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_MPEG2</td>
<td>A bitwise OR of the DXVA_VideoChromaSubsampling_Horizontally_Cosited and DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes values that are used with 4:2:0 data.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_ProgressiveChroma</td>
<td>Specifies that the video chroma subsampling is progressive chroma.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_Unknown</td>
<td>Specifies that the video chroma subsampling is not specified.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_Vertically_AlignedChromaPlanes</td>
<td>Specifies that the Pb and Pr (or Cb and Cr) planes have the same phase alignment. This enumerator can only be set to 0 in the <b>VideoChromaSubsampling</b> member of the <a href="..\dxva\ns-dxva-_dxva_extendedformat.md">DXVA_ExtendedFormat</a> structure if the data is vertically cosited.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsampling_Vertically_Cosited</td>
<td>Specifies that chroma samples are aligned on multiples of the luma samples vertically.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsamplingMask</td>
<td>Specifies the video chroma subsampling mask. 4 (0x00000F00) bits of a DWORD can be used to specify video chroma subsampling.</td>
</tr>

<tr>
<td>DXVA_VideoChromaSubsamplingShift</td>
<td>Specifies to shift bits by 8 positions (DXVA_ExtColorData_ShiftBase + 0, or 8 + 0).</td>
</tr>
</table>

## Remarks

The enumerators of DXVA_VideoChromaSubsampling can be ORed together to create a value in the <b>VideoChromaSubsampling</b> member of the <a href="..\dxva\ns-dxva-_dxva_extendedformat.md">DXVA_ExtendedFormat</a> structure.

Cosite variations indicate that the chroma samples are aligned with the luma samples. Typically, 4:2:0 data with chroma is aligned in one or more directions with the luma data. Note that 4:4:4, 4:2:2 and 4:1:1 data are always cosited in both directions.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dxva.h (include Dxva.h) |

## See Also

<dl>
<dt>
<a href="..\dxva\ns-dxva-_dxva_extendedformat.md">DXVA_ExtendedFormat</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXVA_VideoChromaSubsampling enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>