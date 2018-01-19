---
UID : NS:d3dkmddi._D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS
title : _D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS
author : windows-driver-content
description : Indicates how a kernel mode display-only driver (KMDOD) is to perform a present operation.
old-location : display\d3dkmt_present_display_only_flags.htm
old-project : display
ms.assetid : a45dfdeb-06d2-49c8-a6e1-f42a43857492
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS, D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS
req.alt-loc : D3dkmddi.h
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
req.typenames : D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS
---

# _D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS structure
Indicates how a kernel mode display-only driver (KMDOD) is to perform a present operation.

## Syntax
````
typedef struct _D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS {
  union {
    struct {
      UINT Rotate  :1;
      UINT Reserved  :31;
    };
    UINT   Value;
  };
} D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS;
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
<a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_present_path.md">D3DKMDT_VIDPN_PRESENT_PATH</a>
</dt>
<dt>
<a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_present_path_transformation.md">D3DKMDT_VIDPN_PRESENT_PATH_TRANSFORMATION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMT_PRESENT_DISPLAY_ONLY_FLAGS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>