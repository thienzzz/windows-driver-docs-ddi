---
UID : NS:acpiioct._ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER
title : _ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER
author : windows-driver-content
description : This topic describes the ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER structure.
old-location : acpi\acpi_manipulate_global_lock_buffer.htm
old-project : acpi
ms.assetid : 841CC16D-BDFC-4A3F-9DDD-940A591EBEF2
ms.author : windowsdriverdev
ms.date : 12/31/2017
ms.keywords : _ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER, ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER, *PACPI_MANIPULATE_GLOBAL_LOCK_BUFFER
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : acpiioct.h
req.include-header : Acpiioct.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER
req.alt-loc : Acpiioct.h
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
req.typenames : ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER, *PACPI_MANIPULATE_GLOBAL_LOCK_BUFFER
---

# _ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER structure
This topic describes the  <b>ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER</b> structure.

## Syntax
````
typedef struct _ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER {
  ULONG Signature;
  PVOID LockObject;
} ACPI_MANIPULATE_GLOBAL_LOCK_BUFFER, *PACPI_MANIPULATE_GLOBAL_LOCK_BUFFER;
````

## Members

        
            `LockObject`

            Defines the <b>PVOID</b> member <b>LockObject</b>.
        
            `Signature`

            Defines the <b>ULONG</b> member <b>Signature</b>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | acpiioct.h (include Acpiioct.h) |