---
UID : NS:d3dkmddi._DXGKCB_GETHANDLEDATAFLAGS
title : _DXGKCB_GETHANDLEDATAFLAGS
author : windows-driver-content
description : The DXGKCB_GETHANDLEDATAFLAGS structure indicates if allocations belong to a resource.
old-location : display\dxgkcb_gethandledataflags.htm
old-project : display
ms.assetid : 01689a2f-115a-4db8-b53d-38717c10a0ff
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGKCB_GETHANDLEDATAFLAGS, DXGKCB_GETHANDLEDATAFLAGS
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
req.alt-api : DXGKCB_GETHANDLEDATAFLAGS
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
req.typenames : DXGKCB_GETHANDLEDATAFLAGS
---

# _DXGKCB_GETHANDLEDATAFLAGS structure
The DXGKCB_GETHANDLEDATAFLAGS structure indicates if allocations belong to a resource.

## Syntax
````
typedef struct _DXGKCB_GETHANDLEDATAFLAGS {
  union {
    struct {
      UINT DeviceSpecific  :1;
      UINT Reserved  :31;
    };
    UINT Value;
  };
} DXGKCB_GETHANDLEDATAFLAGS;
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
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkargcb_gethandledata.md">DXGKARGCB_GETHANDLEDATA</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGKCB_GETHANDLEDATAFLAGS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>