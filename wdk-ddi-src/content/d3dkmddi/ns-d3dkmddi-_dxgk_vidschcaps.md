---
UID : NS:d3dkmddi._DXGK_VIDSCHCAPS
title : _DXGK_VIDSCHCAPS
author : windows-driver-content
description : The DXGK_VIDSCHCAPS structure identifies the graphics processing unit (GPU) scheduling capabilities, in bit-field flags, that a driver can support.
old-location : display\dxgk_vidschcaps.htm
old-project : display
ms.assetid : 714741b5-aec1-4d79-8199-00e8d97e6637
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_VIDSCHCAPS, DXGK_VIDSCHCAPS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Available beginning with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_VIDSCHCAPS
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
req.typenames : DXGK_VIDSCHCAPS
---

# _DXGK_VIDSCHCAPS structure
The DXGK_VIDSCHCAPS structure identifies the graphics processing unit (GPU) scheduling capabilities, in bit-field flags, that a driver can support.

## Syntax
````
typedef struct _DXGK_VIDSCHCAPS {
  union {
    struct {
      UINT MultiEngineAware  :1;
      UINT VSyncPowerSaveAware  :1;
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WIN8)
      UINT PreemptionAware  :1;
      UINT NoDmaPatching  :1;
      UINT CancelCommandAware  :1;
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WDDM2_0)
      UINT No64BitAtomics  :1;
      UINT Reserved  :26;
#else 
      UINT Reserved  :27;
#endif 
#else 
      UINT Reserved  :30;
#endif 
    };
    UINT Value;
  };
} DXGK_VIDSCHCAPS;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |

    ## See Also

        <dl>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_cancelcommand.md">DxgkDdiCancelCommand</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createcontext.md">DxgkDdiCreateContext</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_destroycontext.md">DxgkDdiDestroyContext</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_patch.md">DxgkDdiPatch</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_present.md">DxgkDdiPresent</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_render.md">DxgkDdiRender</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGK_VIDSCHCAPS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>