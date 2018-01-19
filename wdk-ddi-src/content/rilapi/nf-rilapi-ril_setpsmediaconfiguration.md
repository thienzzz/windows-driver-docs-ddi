---
UID : NF:rilapi.RIL_SetPSMediaConfiguration
title : RIL_SetPSMediaConfiguration function
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\ril_setpsmediaconfiguration.htm
old-project : netvista
ms.assetid : 66fa9900-0195-4ec0-b181-6f791247422c
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RIL_SetPSMediaConfiguration
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
req.alt-api : RIL_SetPSMediaConfiguration
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


# RIL_SetPSMediaConfiguration function
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax

````
HRESULT  RIL_SetPSMediaConfiguration(
   HRIL                               hRil,
   LPVOID                             lpContext,
   const LPRILPSMEDIACONFIGURATIONSET pConfigurationSet
);
````

## Parameters

`hRil`



`lpContext`



`pConfigurationSet`




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