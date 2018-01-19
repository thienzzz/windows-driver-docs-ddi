---
UID : NF:rilapi.RIL_ManageCalls
title : RIL_ManageCalls function
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\ril_managecalls.htm
old-project : netvista
ms.assetid : d94e3b80-b151-4b3a-a37d-bfba2850b28f
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RIL_ManageCalls
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
req.alt-api : RIL_ManageCalls
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


# RIL_ManageCalls function
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax

````
HRESULT  RIL_ManageCalls(
   HRIL                               hRil,
   LPVOID                             lpContext,
   DWORD                              dwExecutor,
   RILMANAGECALLPARAMSCOMMAND         dwCommand,
   DWORD                              dwID,
   const LPRILCALLMEDIAOFFERANSWERSET lprcmOfferAnswer,
   const LPRILADDRESS                 lpraAddress,
   RILCALLRTTACTION                   dwRTTAction
);
````

## Parameters

`hRil`



`lpContext`



`dwExecutor`



`dwCommand`



`dwID`



`lprcmOfferAnswer`



`lpraAddress`



`dwRTTAction`




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