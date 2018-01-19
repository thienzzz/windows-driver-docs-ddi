---
UID : NS:ntddrilapitypes.RILCALLWAITINGINFO
title : RILCALLWAITINGINFO
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilcallwaitinginfo.htm
old-project : netvista
ms.assetid : 526ce708-93bb-43f2-9d78-b3e8360e01da
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILCALLWAITINGINFO, *LPRILCALLWAITINGINFO, RILCALLWAITINGINFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddrilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILCALLWAITINGINFO
req.alt-loc : ntddrilapitypes.h
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
req.typenames : "*LPRILCALLWAITINGINFO, RILCALLWAITINGINFO"
---

# RILCALLWAITINGINFO structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILCALLWAITINGINFO {
  DWORD               cbSize;
  DWORD               dwParams;
  DWORD               dwExecutor;
  RILCALLTYPE         dwCallType;
  RILREMOTEPARTYINFO  rrpiCallerInfo;
} RILCALLWAITINGINFO, RILCALLWAITINGINFO;
````

## Members

        
            `cbSize`

            
        
            `dwCallType`

            
        
            `dwExecutor`

            
        
            `dwParams`

            
        
            `rrpiCallerInfo`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |