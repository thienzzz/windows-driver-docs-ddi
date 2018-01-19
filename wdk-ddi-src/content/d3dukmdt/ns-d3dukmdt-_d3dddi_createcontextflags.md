---
UID : NS:d3dukmdt._D3DDDI_CREATECONTEXTFLAGS
title : _D3DDDI_CREATECONTEXTFLAGS
author : windows-driver-content
description : The D3DDDI_CREATECONTEXTFLAGS structure describes how to create a context in a call to the pfnCreateContextCb function.
old-location : display\d3dddi_createcontextflags.htm
old-project : display
ms.assetid : e450f85c-4c73-44a8-9d0a-da2c212c87c9
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DDDI_CREATECONTEXTFLAGS, D3DDDI_CREATECONTEXTFLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dukmdt.h
req.include-header : D3dumddi.h, D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DDDI_CREATECONTEXTFLAGS
req.alt-loc : d3dukmdt.h
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
req.typenames : D3DDDI_CREATECONTEXTFLAGS
---

# _D3DDDI_CREATECONTEXTFLAGS structure
The D3DDDI_CREATECONTEXTFLAGS structure describes how to create a context in a call to the <a href="https://msdn.microsoft.com/f3f5d6bc-3bc6-4214-830a-cffff01069cc">pfnCreateContextCb</a> function.

## Syntax
````
typedef struct _D3DDDI_CREATECONTEXTFLAGS {
  union {
    struct {
      UINT NullRendering  :1;
      UINT InitialData  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DDDI_CREATECONTEXTFLAGS;
````

## Members



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dukmdt.h (include D3dumddi.h, D3dkmddi.h) |

    ## See Also

        <dl>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_d3dddicb_createcontext.md">D3DDDICB_CREATECONTEXT</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/f3f5d6bc-3bc6-4214-830a-cffff01069cc">pfnCreateContextCb</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DDDI_CREATECONTEXTFLAGS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>