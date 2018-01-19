---
UID : NS:d3dkmthk._D3DKMT_QUERYPROTECTEDSESSIONSTATUS
title : _D3DKMT_QUERYPROTECTEDSESSIONSTATUS
author : windows-driver-content
description : Used to query the status of the protected session.
old-location : display\d3dkmt-queryprotectedsessionstatus.htm
old-project : display
ms.assetid : c49b1c12-8757-4d15-807d-fdb963746810
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_QUERYPROTECTEDSESSIONSTATUS, D3DKMT_QUERYPROTECTEDSESSIONSTATUS
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
req.alt-api : D3DKMT_QUERYPROTECTEDSESSIONSTATUS
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
req.typenames : D3DKMT_QUERYPROTECTEDSESSIONSTATUS
---

# _D3DKMT_QUERYPROTECTEDSESSIONSTATUS structure
Used to query the status of the protected session.

## Syntax
````
typedef struct _D3DKMT_QUERYPROTECTEDSESSIONSTATUS {
  D3DKMT_HANDLE                   hHandle;
  D3DKMT_PROTECTED_SESSION_STATUS Status;
} D3DKMT_QUERYPROTECTEDSESSIONSTATUS;
````

## Members

        
            `hHandle`

            The handle of the protected session.
        
            `Status`

            The status of the protected session.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h |