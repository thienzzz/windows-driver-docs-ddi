---
UID : NF:rilapi.RIL_SendUiccToolkitCmdResponse
title : RIL_SendUiccToolkitCmdResponse function
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\ril_senduicctoolkitcmdresponse.htm
old-project : netvista
ms.assetid : 400e2172-803c-4b6c-a41e-3c322077ffa4
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RIL_SendUiccToolkitCmdResponse
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
req.alt-api : RIL_SendUiccToolkitCmdResponse
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


# RIL_SendUiccToolkitCmdResponse function
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax

````
HRESULT  RIL_SendUiccToolkitCmdResponse(
   HRIL         hRil,
   LPVOID       lpContext,
   DWORD        dwSlotIndex,
   const LPBYTE pbDetails,
   DWORD        dwDetailSize
);
````

## Parameters

`hRil`



`lpContext`



`dwSlotIndex`



`pbDetails`



`dwDetailSize`




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