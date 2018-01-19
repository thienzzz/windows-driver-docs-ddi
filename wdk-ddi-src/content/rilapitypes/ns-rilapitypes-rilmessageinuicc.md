---
UID : NS:rilapitypes.RILMESSAGEINUICC
title : RILMESSAGEINUICC
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilmessageinuicc_2.htm
old-project : netvista
ms.assetid : 2a956b25-1cf5-4a51-bc60-c4a7a7f70e2c
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILMESSAGEINUICC, RILMESSAGEINUICC, *LPRILMESSAGEINUICC
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : rilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILMESSAGEINUICC
req.alt-loc : rilapitypes.h
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
req.typenames : RILMESSAGEINUICC, *LPRILMESSAGEINUICC
req.product : Windows 10 or later.
---

# RILMESSAGEINUICC structure
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef struct _RILMESSAGEINUICC {
  DWORD     cbSize;
  DWORD     dwExecutor;
  HUICCAPP  hUiccApp;
  DWORD     dwIndex;
} RILMESSAGEINUICC, RILMESSAGEINUICC;
````

## Members

        
            `cbSize`

            
        
            `dwExecutor`

            
        
            `dwIndex`

            
        
            `hUiccApp`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapitypes.h |