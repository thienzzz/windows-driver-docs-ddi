---
UID : NF:kcom.KoRelease
title : KoRelease function
author : windows-driver-content
description : The KoRelease function decrements the reference count for the calling interface on an object.
old-location : stream\korelease.htm
old-project : stream
ms.assetid : 59be582c-0f56-45d8-b407-e588ee0f7f8b
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : KoRelease
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : kcom.h
req.include-header : Kcom.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KoRelease
req.alt-loc : Ks.lib,Ks.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ks.lib
req.dll : 
req.irql : 
req.typenames : CONNECT_DATA, *PCONNECT_DATA
---


# KoRelease function
<i>This function is intended for internal use only.</i>

The <b>KoRelease</b> function decrements the reference count for the calling interface on an object.

## Syntax

````
void KoRelease(
  _In_ REFCLSID ClassId
);
````

## Parameters

`ClassId`

The CLSID of the object whose reference count will be decremented.


## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | kcom.h (include Kcom.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |