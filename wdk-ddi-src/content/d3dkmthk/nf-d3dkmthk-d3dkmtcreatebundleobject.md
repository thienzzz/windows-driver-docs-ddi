---
UID : NF:d3dkmthk.D3DKMTCreateBundleObject
title : D3DKMTCreateBundleObject function
author : windows-driver-content
description : Used to create a bundle object.
old-location : display\d3dkmtcreatebundleobject.htm
old-project : display
ms.assetid : c4d62ccf-606b-457e-a239-1b5189e42657
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3DKMTCreateBundleObject
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : d3dkmthk.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMTCreateBundleObject
req.alt-loc : d3dkmthk.h
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
req.typenames : D3DKMT_DRIVERVERSION
---


# D3DKMTCreateBundleObject function
Used to create a bundle object.

## Syntax

````
NTSTATUS  D3DKMTCreateBundleObject(
  _Inout_ D3DKMT_CREATEBUNDLEOBJECT  *D3dkmt_createbundleobject
);
````

## Parameters

This function has no parameters.

## Return Value

Returns STATUS_SUCCESS if the call has been successfully completed.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |