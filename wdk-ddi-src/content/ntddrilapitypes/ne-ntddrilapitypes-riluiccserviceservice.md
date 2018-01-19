---
UID : NE:ntddrilapitypes.RILUICCSERVICESERVICE
title : RILUICCSERVICESERVICE
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\riluiccserviceservice.htm
old-project : netvista
ms.assetid : 1aeb4642-d718-4e39-a6c7-dc33146c9687
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILUICCSERVICESERVICE, RILUICCSERVICESERVICE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ntddrilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILUICCSERVICESERVICE
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
req.typenames : RILUICCSERVICESERVICE
---

# RILUICCSERVICESERVICE Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILUICCSERVICESERVICE { 
  RIL_UICCOPERATION_SERVICE_BDN,
  RIL_UICCOPERATION_SERVICE_ACL,
  RIL_UICCOPERATION_SERVICE_MAX
} RILUICCSERVICESERVICE;
````

## Constants

<table>

<tr>
<td>RIL_UICCOPERATION_SERVICE_ACL</td>
<td></td>
</tr>

<tr>
<td>RIL_UICCOPERATION_SERVICE_BDN</td>
<td></td>
</tr>

<tr>
<td>RIL_UICCOPERATION_SERVICE_MAX</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddrilapitypes.h |