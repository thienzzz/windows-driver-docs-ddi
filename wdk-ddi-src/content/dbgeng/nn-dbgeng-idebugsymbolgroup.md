---
UID: NN:dbgeng.IDebugSymbolGroup
title: IDebugSymbolGroup
author: windows-driver-content
description: IDebugSymbolGroup interface
old-location: debugger\idebugsymbolgroup.htm
old-project: debugger
ms.assetid: dd629e4a-938e-4db6-b0f3-6dd12a431486
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ComOther_f174a794-e2c2-4d0a-912e-b3de6327ef19.xml, IDebugSymbolGroup, IDebugSymbolGroup interface [Windows Debugging], IDebugSymbolGroup interface [Windows Debugging],described, dbgeng/IDebugSymbolGroup, debugger.idebugsymbolgroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugSymbolGroup
product:
- Windows
targetos: Windows
req.typenames: 
---

# IDebugSymbolGroup interface


## -description




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDebugSymbolGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDebugSymbolGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDebugSymbolGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff537925">AddSymbol</a>
</td>
<td align="left" width="63%">
Adds a symbol to a symbol group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543271">ExpandSymbol</a>
</td>
<td align="left" width="63%">
Adds or removes the children of a symbol from a symbol group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff547975">GetNumberSymbols</a>
</td>
<td align="left" width="63%">
 Returns the number of symbols that are contained in a symbol group.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549121">GetSymbolName</a>
</td>
<td align="left" width="63%">
Returns the name of a symbol in a symbol group.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff549146">GetSymbolParameters</a>
</td>
<td align="left" width="63%">
Returns the symbol parameters that describe the specified symbols in a symbol group.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff553191">OutputAsType</a>
</td>
<td align="left" width="63%">
Changes the type of a symbol in a symbol group. The symbol's entry is updated to represent the new type. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff553264">OutputSymbols</a>
</td>
<td align="left" width="63%">
Prints the specified symbols to the debugger console.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554510">RemoveSymbolByIndex</a>
</td>
<td align="left" width="63%">
Removes the specified symbol from a symbol group.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554518">RemoveSymbolByName</a>
</td>
<td align="left" width="63%">
 Removes the specified symbol from a symbol group.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff561457">WriteSymbol</a>
</td>
<td align="left" width="63%">
Sets the value of the specified symbol.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550846">IDebugSymbolGroup2</a>
 

 

