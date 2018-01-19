---
UID : NS:d3dumddi._DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
title : _DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
author : windows-driver-content
description : The DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure describes data that specifies the color space of the output.
old-location : display\dxvahdddi_blt_state_output_color_space_data.htm
old-project : display
ms.assetid : 411246a5-9486-4194-9fb1-4ec0ba1dd47b
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA, DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA is supported beginning with the Windows 7 operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
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
req.typenames : DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA
---

# _DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure
The DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure describes data that specifies the color space of the output.

## Syntax
````
typedef struct _DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA {
  union {
    struct {
      UINT Usage  :1;
      UINT RGB_Range  :1;
      UINT YCbCr_Matrix  :1;
      UINT YCbCr_xvYCC  :1;
      UINT Nominal_Range  :2;
      UINT Reserved  :26;
    };
    UINT   Value;
  };
} DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA;
````

## Members


    ## Remarks
        If the driver does not set the DXVAHDDDI_DEVICE_CAPS_xvYCC value in the <b>DeviceCaps</b> member of the <a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_vpdevcaps.md">DXVAHDDDI_VPDEVCAPS</a> structure when the driver's <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a> function is called with the D3DDDICAPS_DXVAHD_GETVPDEVCAPS value set, the output ignores the <b>YCbCr_xvYCC</b> member.

Either RGB or YCbCr flags that correspond to the color space of the output format are referred. However, the driver might have to perform the color space conversion to the background color, in which case both RGB and YCbCr flags are referred.

An application should set the <b>Usage</b> member such that the driver can perform the optimal color conversion. If usage is set to video playback (<b>Usage</b>=0), the driver can use a sophisticated algorism to maximize the presentation experience (for example, auto gain control or dynamic gamma mapping is used to maximize the dynamic range while the super white is preserved). If the usage is set to video processing (<b>Usage</b>=1), the driver should accept the values that are set in the other members of DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA and perform the conversion exactly as specified in the other members.

RGB output can be out of [0.0, 1.0] range ([0, 255], when 8-bit presentation is used) in the event that the output RGB type is a wide range format (for example, XR_BIAS, FP16, or FP32 format). Especially when the input stream is extended YCbCr (xvYCC), the RGB output range becomes wider than sRGB color space.

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
<a href="..\d3dumddi\ne-d3dumddi-_dxvahdddi_nominal_range.md">DXVAHDDDI_NOMINAL_RANGE</a>
</dt>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_dxvahdddi_vpdevcaps.md">DXVAHDDDI_VPDEVCAPS</a>
</dt>
<dt>
<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXVAHDDDI_BLT_STATE_OUTPUT_COLOR_SPACE_DATA structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>