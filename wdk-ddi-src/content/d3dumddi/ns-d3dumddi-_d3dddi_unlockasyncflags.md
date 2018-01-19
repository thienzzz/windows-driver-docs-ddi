---
UID : NS:d3dumddi._D3DDDI_UNLOCKASYNCFLAGS
title : _D3DDDI_UNLOCKASYNCFLAGS
author : windows-driver-content
description : The D3DDDI_UNLOCKASYNCFLAGS structure identifies how to unlock a resource.
old-location : display\d3dddi_unlockasyncflags.htm
old-project : display
ms.assetid : c31e4a4e-7bc7-43a2-8f86-e79012064fa2
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DDDI_UNLOCKASYNCFLAGS, D3DDDI_UNLOCKASYNCFLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dumddi.h
req.include-header : D3dumddi.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DDDI_UNLOCKASYNCFLAGS
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
req.typenames : D3DDDI_UNLOCKASYNCFLAGS
---

# _D3DDDI_UNLOCKASYNCFLAGS structure
The D3DDDI_UNLOCKASYNCFLAGS structure identifies how to unlock a resource.

## Syntax
````
typedef struct _D3DDDI_UNLOCKASYNCFLAGS {
  union {
    struct {
      UINT NotifyOnly  :1;
      UINT Reserved  :31;
    };
    UINT   Value;
  };
} D3DDDI_UNLOCKASYNCFLAGS;
````

## Members



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
<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_unlock.md">D3DDDIARG_UNLOCK</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DDDI_UNLOCKASYNCFLAGS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>