---
UID : NF:iddcx.IddCxSwapChainGetMoveRegions
title : IddCxSwapChainGetMoveRegions function
author : windows-driver-content
description : n OS callback function the driver calls when it wants retrieve the move regions for the current frame.
old-location : display\iddcxswapchaingetmoveregions.htm
old-project : display
ms.assetid : ae8257a6-4d4c-446e-b144-1adfe0a28e50
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : IddCxSwapChainGetMoveRegions
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : iddcx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IddCxSwapChainGetMoveRegions
req.alt-loc : iddcx.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : _Must_inspect_result_
req.typenames : 
---


# IddCxSwapChainGetMoveRegions function
n OS callback function the driver calls when it wants retrieve the move regions for the current frame

## Syntax

````
HRESULT IddCxSwapChainGetMoveRegions(
  _In_        IDDCX_SWAPCHAIN           SwapChainObject,
  _In_  const IDARG_IN_GETMOVEREGIONS*  pInArgs,
  _Out_       IDARG_OUT_GETMOVEREGIONS* pOutArgs
);
````

## Parameters

`SwapChainObject`

The swap-chain object whose current frame is being queried.

`pInArgs`

Input arguments of the function

`pOutArgs`

Output arguments of the function


## Return Value

(NTSTATUS) The method returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method may return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | iddcx.h |
| **Library** |  |
| **IRQL** | _Must_inspect_result_ |
| **DDI compliance rules** |  |