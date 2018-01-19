---
UID : NE:d3dumddi._DXVADDI_SAMPLEFORMAT
title : _DXVADDI_SAMPLEFORMAT
author : windows-driver-content
description : The DXVADDI_SAMPLEFORMAT enumeration type contains values that identify how a video frame is sampled.
old-location : display\dxvaddi_sampleformat.htm
old-project : display
ms.assetid : 23482cdc-6412-4309-805e-a439d8e81b59
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXVADDI_SAMPLEFORMAT, DXVADDI_SAMPLEFORMAT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXVADDI_SAMPLEFORMAT
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
req.typenames : DXVADDI_SAMPLEFORMAT
---

# _DXVADDI_SAMPLEFORMAT Enumeration
The DXVADDI_SAMPLEFORMAT enumeration type contains values that identify how a video frame is sampled.

## Syntax
````
typedef enum _DXVADDI_SAMPLEFORMAT { 
  DXVADDI_SampleFormatMask                 = 0x00FF,
  DXVADDI_SampleUnknown                    = 0,
  DXVADDI_SampleProgressiveFrame           = 2,
  DXVADDI_SampleFieldInterleavedEvenFirst  = 3,
  DXVADDI_SampleFieldInterleavedOddFirst   = 4,
  DXVADDI_SampleFieldSingleEven            = 5,
  DXVADDI_SampleFieldSingleOdd             = 6,
  DXVADDI_SampleSubStream                  = 7
} DXVADDI_SAMPLEFORMAT;
````

## Constants

<table>

<tr>
<td>DXVADDI_SampleFieldInterleavedEvenFirst</td>
<td>The sample contains two interleaved fields; the even field is temporally first.</td>
</tr>

<tr>
<td>DXVADDI_SampleFieldInterleavedOddFirst</td>
<td>The sample contains two interleaved fields; the odd field is temporally first.</td>
</tr>

<tr>
<td>DXVADDI_SampleFieldSingleEven</td>
<td>The sample contains an even interleaved field.</td>
</tr>

<tr>
<td>DXVADDI_SampleFieldSingleOdd</td>
<td>The sample contains an odd interleaved field.</td>
</tr>

<tr>
<td>DXVADDI_SampleFormatMask</td>
<td>The sample format mask. The first 8 (0xFF) bits of a DWORD can be used to specify input sample format.</td>
</tr>

<tr>
<td>DXVADDI_SampleProgressiveFrame</td>
<td>The sample contains a progressive frame.</td>
</tr>

<tr>
<td>DXVADDI_SampleSubStream</td>
<td>The sample contains a video substream.</td>
</tr>

<tr>
<td>DXVADDI_SampleUnknown</td>
<td>The sample format is unknown.</td>
</tr>
</table>

## Remarks

One of the values of DXVADDI_SAMPLEFORMAT can be specified in the <b>SampleFormat</b> member of the <a href="..\d3dumddi\ns-d3dumddi-_dxvaddi_extendedformat.md">DXVADDI_EXTENDEDFORMAT</a> structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dumddi.h (include D3dumddi.h) |

## See Also

<dl>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_dxvaddi_extendedformat.md">DXVADDI_EXTENDEDFORMAT</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXVADDI_SAMPLEFORMAT enumeration%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>