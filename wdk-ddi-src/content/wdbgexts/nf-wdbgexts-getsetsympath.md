---
UID : NF:wdbgexts.GetSetSympath
title : GetSetSympath function
author : windows-driver-content
description : The GetSetSympath function can be used to either get or set the symbol search path.
old-location : debugger\getsetsympath.htm
old-project : debugger
ms.assetid : 2c7392c2-49c8-4b27-addc-0200eabbe87e
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : GetSetSympath
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdbgexts.h
req.include-header : Wdbgexts.h, Dbgeng.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : GetSetSympath
req.alt-loc : wdbgexts.h
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
req.typenames : EXT_TDOP
req.product : Windows 10 or later.
---


# GetSetSympath function
The <b>GetSetSympath</b> function can be used to either get or set the symbol search path.

## Syntax

````
__inline VOID GetSetSympath(
  _In_      PSTR Arg,
  _Out_opt_ PSTR Result,
  _In_      int  Length
);
````

## Parameters

`Arg`

Specifies the new search path. If this argument is <b>NULL</b> or the string is empty, the search path is not set and the current setting is returned in <i>Result</i>.

`OPTIONAL`



`Length`

Specifies the size of the buffer for storing the result.


## Return Value

None

## Remarks

When the symbol path is changed, a call to <b>ReloadSymbols</b> is made implicitly.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdbgexts.h (include Wdbgexts.h, Dbgeng.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |