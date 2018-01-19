---
UID : NF:wiautil.wiauDbgLegacyTrace2
title : wiauDbgLegacyTrace2 function
author : windows-driver-content
description : The wiauDbgLegacyTrace2 function logs a trace message.
old-location : image\wiaudbglegacytrace2.htm
old-project : image
ms.assetid : 911a7089-d4ac-4da0-8be6-a3a36567635c
ms.author : windowsdriverdev
ms.date : 1/17/2018
ms.keywords : wiauDbgLegacyTrace2
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wiautil.h
req.include-header : Wiautil.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows XP and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : wiauDbgLegacyTrace2
req.alt-loc : Wiautil.h
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
req.typenames : SKIP_AMOUNT
req.product : Windows 10 or later.
---


# wiauDbgLegacyTrace2 function
The <b>wiauDbgLegacyTrace2</b> function logs a trace message.

## Syntax

````
inline void __stdcall wiauDbgLegacyTrace2(
   HINSTANCE   hInstance,
   LPCSTR      fmt, ...
);
````

## Parameters

`hInstance`

Specifies the handle to the DLL instance.

`fmt`



``




## Return Value

None

## Remarks

The <b>wiauDbgLegacyTrace2</b> function is identical to the <a href="..\wiautil\nf-wiautil-wiaudbgtrace.md">wiauDbgTrace</a> function except that the former has a parameter that specifies the handle to the DLL instance and the latter has a parameter used to identify the function or method that is active when the function is called.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wiautil.h (include Wiautil.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wiautil\nf-wiautil-wiaudbgtrace.md">wiauDbgTrace</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [image\image]:%20wiauDbgLegacyTrace2 function%20 RELEASE:%20(1/17/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>