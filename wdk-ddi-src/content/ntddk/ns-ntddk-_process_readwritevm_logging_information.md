---
UID : NS:ntddk._PROCESS_READWRITEVM_LOGGING_INFORMATION
title : _PROCESS_READWRITEVM_LOGGING_INFORMATION
author : windows-driver-content
description : Stores options for read/write access for telemetry per process.
old-location : kernel\process_readwritevm_logging_information.htm
old-project : kernel
ms.assetid : F1C769FD-D05F-4C23-A91E-FAEE8EA029EC
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _PROCESS_READWRITEVM_LOGGING_INFORMATION, PROCESS_READWRITEVM_LOGGING_INFORMATION, *PPROCESS_READWRITEVM_LOGGING_INFORMATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddk.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10, version 1709
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PROCESS_READWRITEVM_LOGGING_INFORMATION
req.alt-loc : Ntddk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : PROCESS_READWRITEVM_LOGGING_INFORMATION, *PPROCESS_READWRITEVM_LOGGING_INFORMATION
---

# _PROCESS_READWRITEVM_LOGGING_INFORMATION structure
Stores options for read/write access for  telemetry per process.

## Syntax
````
typedef union _PROCESS_READWRITEVM_LOGGING_INFORMATION {
  UCHAR Flags;
  struct {
    UCHAR EnableReadVmLogging  :1;
    UCHAR EnableWriteVmLogging  :1;
    UCHAR Unused  :6;
  };
} PROCESS_READWRITEVM_LOGGING_INFORMATION, *PPROCESS_READWRITEVM_LOGGING_INFORMATION;
````

## Members

        
            `Flags`

            Reserved.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h |