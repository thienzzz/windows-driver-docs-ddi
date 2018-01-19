---
UID : NS:d3dkmdt._D3DKMDT_GAMMA_RAMP
title : _D3DKMDT_GAMMA_RAMP
author : windows-driver-content
description : The D3DKMDT_GAMMA_RAMP structure contains descriptive information about a gamma lookup table and a pointer to the lookup table.
old-location : display\d3dkmdt_gamma_ramp.htm
old-project : display
ms.assetid : 3a875a1e-ef4f-4851-9329-f1fd2aca261f
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMDT_GAMMA_RAMP, D3DKMDT_GAMMA_RAMP
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmdt.h
req.include-header : D3dkmdt.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMDT_GAMMA_RAMP
req.alt-loc : d3dkmdt.h
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
req.typenames : D3DKMDT_GAMMA_RAMP
---

# _D3DKMDT_GAMMA_RAMP structure
The D3DKMDT_GAMMA_RAMP structure contains descriptive information about a gamma lookup table and a pointer to the lookup table.

## Syntax
````
typedef struct _D3DKMDT_GAMMA_RAMP {
  D3DDDI_GAMMARAMP_TYPE Type;
  SIZE_T                DataSize;
  union {
    D3DDDI_GAMMA_RAMP_RGB256x3x16   *pRgb256x3x16;
    D3DDDI_GAMMA_RAMP_DXGI_1        *pDxgi1;
    D3DDDI_3x4_COLORSPACE_TRANSFORM *p3x4;
    VOID                            *pRaw;
  } Data;
} D3DKMDT_GAMMA_RAMP;
````

## Members

        
            `Data`

            [in] A union that contains one of the following ways to access the lookup table data depending on the value in the Type member:
        
            `DataSize`

            The size, in bytes, of the lookup table pointed to by <i>Data</i>.
        
            `Type`

            A <a href="..\d3dukmdt\ne-d3dukmdt-_d3dddi_gammaramp_type.md">D3DDDI_GAMMARAMP_TYPE</a> enumerator that specifies the format of the lookup table.

    ## Remarks
        The <b>GammaRamp</b> member of the <a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_present_path.md">D3DKMDT_VIDPN_PRESENT_PATH</a> structure is a D3DKMDT_GAMMA_RAMP structure.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmdt.h (include D3dkmdt.h) |