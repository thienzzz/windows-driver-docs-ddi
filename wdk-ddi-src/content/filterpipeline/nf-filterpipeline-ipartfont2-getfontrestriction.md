---
UID : NF:filterpipeline.IPartFont2.GetFontRestriction
title : IPartFont2::GetFontRestriction method
author : windows-driver-content
description : .
old-location : print\ipartfont2_getfontrestriction.htm
old-project : print
ms.assetid : C6289E38-281A-46A2-8E28-138A20BF6684
ms.author : windowsdriverdev
ms.date : 1/8/2018
ms.keywords : IPartFont2, IPartFont2::GetFontRestriction, GetFontRestriction
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : filterpipeline.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IPartFont2.GetFontRestriction
req.alt-loc : Filterpipeline.h
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
req.typenames : EXpsFontRestriction
---


# GetFontRestriction method


## Syntax

````
HRESULT GetFontRestriction(
  [out] EXpsFontRestriction *pRestriction
);
````

## Parameters

`pRestriction`




## Return Value

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | filterpipeline.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\filterpipeline\nn-filterpipeline-ipartfont2.md">IPartFont2</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPartFont2::GetFontRestriction method%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>