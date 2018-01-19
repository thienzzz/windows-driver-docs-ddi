---
UID : NS:d3dkmddi._DXGK_CREATEDEVICEFLAGS
title : _DXGK_CREATEDEVICEFLAGS
author : windows-driver-content
description : The DXGK_CREATEDEVICEFLAGS structure identifies how to create devices.
old-location : display\dxgk_createdeviceflags.htm
old-project : display
ms.assetid : 31dc1493-a7c9-4ca0-b718-98224d9c5675
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_CREATEDEVICEFLAGS, DXGK_CREATEDEVICEFLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_CREATEDEVICEFLAGS
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
req.typenames : DXGK_CREATEDEVICEFLAGS
---

# _DXGK_CREATEDEVICEFLAGS structure
The DXGK_CREATEDEVICEFLAGS structure identifies how to create devices.

## Syntax
````
typedef struct _DXGK_CREATEDEVICEFLAGS {
  union {
    struct {
      UINT SystemDevice  :1;
      UINT GdiDevice  :1;
      UINT Reserved  :29;
      UINT DXGK_DEVICE_RESERVED0  :1;
    };
    UINT Value;
  };
} DXGK_CREATEDEVICEFLAGS;
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
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_createdevice.md">DXGKARG_CREATEDEVICE</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createdevice.md">DxgkDdiCreateDevice</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGK_CREATEDEVICEFLAGS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>