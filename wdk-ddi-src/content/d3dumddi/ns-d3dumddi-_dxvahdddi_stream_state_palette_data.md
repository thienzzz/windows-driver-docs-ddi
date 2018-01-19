---
UID : NS:d3dumddi._DXVAHDDDI_STREAM_STATE_PALETTE_DATA
title : _DXVAHDDDI_STREAM_STATE_PALETTE_DATA
author : windows-driver-content
description : The DXVAHDDDI_STREAM_STATE_PALETTE_DATA structure describes stream-state data that specifies the palette entries of the input.
old-location : display\dxvahdddi_stream_state_palette_data.htm
old-project : display
ms.assetid : b71f3793-7856-4558-b205-7facf6d83a8c
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXVAHDDDI_STREAM_STATE_PALETTE_DATA, DXVAHDDDI_STREAM_STATE_PALETTE_DATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : DXVAHDDDI_STREAM_STATE_PALETTE_DATA is supported beginning with the Windows 7 operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXVAHDDDI_STREAM_STATE_PALETTE_DATA
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
req.typenames : DXVAHDDDI_STREAM_STATE_PALETTE_DATA
---

# _DXVAHDDDI_STREAM_STATE_PALETTE_DATA structure
The DXVAHDDDI_STREAM_STATE_PALETTE_DATA structure describes stream-state data that specifies the palette entries of the input.

## Syntax
````
typedef struct _DXVAHDDDI_STREAM_STATE_PALETTE_DATA {
  UINT     Count;
  D3DCOLOR *pEntries;
} DXVAHDDDI_STREAM_STATE_PALETTE_DATA;
````

## Members

        
            `Count`

            [in] The number of palette entries in the array that the <b>pEntries</b> member specifies. The default value is 0.
        
            `pEntries`

            [in] An array of palette entries in either D3DFMT_A8R8G8B8 or "AYUV" <a href="wdkgloss.f#wdkgloss.fourcc#wdkgloss.fourcc"><i>FOURCC</i></a> format type. <b>pEntries</b> is set to <b>NULL</b> to retrieve the number of palette entries. The default value is <b>NULL</b>.

    ## Remarks
        The 4-bit palletized "AYUV" FOURCC formats, "AI44", and "IA44" uses the first 16 entries.

The 8-bit palletized "AYUV" FOURCC format, "AI88", D3DFMT_A8P8, and D3DFMT_P8 formats uses the first 256 entries.

If a pixel has a palette index greater than the entries, the driver assumes that the palette entry is white with opaque alpha. Full range RGB is D3DCOLOR_ARGB(255, 255, 255, 255), and YCbCr is D3DCOLOR_AYUV(255, 235, 128, 128).

The Direct3D runtime maintains all the palette entries. However, the driver might truncate the palette entries array to the maximum entries required for the supported palletized format.

The alpha value of each entry is used for the alpha blending.

If the driver does not set the DXVAHDDDI_FEATURE_CAPS_ALPHA_PALETTE value in the <b>FeatureCaps</b> member of the <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_vpdevcaps.md">DXVAHDDDI_VPDEVCAPS</a> structure when the driver's <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a> function is called with the D3DDDICAPS_DXVAHD_GETVPDEVCAPS value set, every palette entry must have the alpha value set to opaque (0xFF); otherwise, the driver's <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_dxvahd_setvideoprocessstreamstate.md">SetVideoProcessStreamState</a> function returns an error.

For more information about alpha blending, see <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_stream_state_alpha_data.md">DXVAHDDDI_STREAM_STATE_ALPHA_DATA</a>.

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
<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_stream_state_alpha_data.md">DXVAHDDDI_STREAM_STATE_ALPHA_DATA</a>
</dt>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_vpdevcaps.md">DXVAHDDDI_VPDEVCAPS</a>
</dt>
<dt>
<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a>
</dt>
<dt>
<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_dxvahd_setvideoprocessstreamstate.md">SetVideoProcessStreamState</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXVAHDDDI_STREAM_STATE_PALETTE_DATA structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>