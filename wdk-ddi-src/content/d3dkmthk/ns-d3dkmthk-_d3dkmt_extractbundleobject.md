---
UID : NS:d3dkmthk._D3DKMT_EXTRACTBUNDLEOBJECT
title : _D3DKMT_EXTRACTBUNDLEOBJECT
author : windows-driver-content
description : Used to extract the bundle object.
old-location : display\d3dkmt-extractbundleobject.htm
old-project : display
ms.assetid : 85112ddb-47e6-4874-bd64-a7e4d7ca0fd3
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_EXTRACTBUNDLEOBJECT, D3DKMT_EXTRACTBUNDLEOBJECT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmthk.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMT_EXTRACTBUNDLEOBJECT
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
req.typenames : D3DKMT_EXTRACTBUNDLEOBJECT
---

# _D3DKMT_EXTRACTBUNDLEOBJECT structure
Used to extract the bundle object.

## Syntax
````
typedef struct _D3DKMT_EXTRACTBUNDLEOBJECT {
  HANDLE hNtBundleHandle;
  UINT   cObjects;
  DWORD  *pdwDesiredAccess;
  HANDLE *phNtHandles;
} D3DKMT_EXTRACTBUNDLEOBJECT;
````

## Members

        
            `cObjects`

            The number of the DXGK object to be unbundled.
        
            `hNtBundleHandle`

            The NT bundle handle.
        
            `pdwDesiredAccess`

            The desired access for each NT handle for DXGK objects.
        
            `phNtHandles`

            The pointer to an array of NT handles for each DXGK object.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h |