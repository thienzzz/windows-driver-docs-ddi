---
UID : NE:ntddstor._STORAGE_DIAGNOSTIC_LEVEL
title : _STORAGE_DIAGNOSTIC_LEVEL
author : windows-driver-content
description : The STORAGE_DIAGNOSTIC_LEVEL enumeration specifies the target type of a storage diagnostic.
old-location : storage\storage_diagnostic_level.htm
old-project : storage
ms.assetid : 6D705DA8-7F45-4C7A-813F-5AE4F5A1D8ED
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _STORAGE_DIAGNOSTIC_LEVEL, STORAGE_DIAGNOSTIC_LEVEL, *PSTORAGE_DIAGNOSTIC_LEVEL
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ntddstor.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows 10, version 1709.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : STORAGE_DIAGNOSTIC_LEVEL
req.alt-loc : ntddstor.h
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
req.typenames : STORAGE_DIAGNOSTIC_LEVEL, *PSTORAGE_DIAGNOSTIC_LEVEL
---

# _STORAGE_DIAGNOSTIC_LEVEL Enumeration
The <b>STORAGE_DIAGNOSTIC_LEVEL</b> enumeration specifies the target type of a storage diagnostic.

## Syntax
````
typedef enum _STORAGE_DIAGNOSTIC_LEVEL { 
  StorageDiagnosticLevelDefault  = 0,
  StorageDiagnosticLevelMax
} STORAGE_DIAGNOSTIC_LEVEL, *PSTORAGE_DIAGNOSTIC_LEVEL;
````

## Constants

<table>

<tr>
<td>StorageDiagnosticLevelDefault</td>
<td>Specifies the default diagnostic level.</td>
</tr>

<tr>
<td>StorageDiagnosticLevelMax</td>
<td>Specifies the max diagnostic level.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddstor.h |