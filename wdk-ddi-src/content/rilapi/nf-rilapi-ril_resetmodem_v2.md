---
UID : NF:rilapi.RIL_ResetModem_V2
title : RIL_ResetModem_V2 function
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\ril_resetmodem_v2.htm
old-project : netvista
ms.assetid : 3ee0ac02-6473-4f1d-9ac7-28f72140cc61
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RIL_ResetModem_V2
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : rilapi.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RIL_ResetModem_V2
req.alt-loc : rilapi.h
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
req.typenames : "*PRH_QUERY_CONNECTION_PROPERTIES_OUTPUT_BUFFER, RH_QUERY_CONNECTION_PROPERTIES_OUTPUT_BUFFER"
req.product : Windows 10 or later.
---


# RIL_ResetModem_V2 function
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax

````
HRESULT  RIL_ResetModem_V2(
   HRIL                       hRil,
   LPVOID                     lpContext,
   const RILRESETMODEMPARAMS  params
);
````

## Parameters

`hRil`



`lpContext`



`params`




## Return Value

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapi.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |