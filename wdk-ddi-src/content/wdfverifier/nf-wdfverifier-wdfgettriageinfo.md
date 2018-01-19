---
UID : NF:wdfverifier.WdfGetTriageInfo
title : WdfGetTriageInfo function
author : windows-driver-content
description : The WdfGetTriageInfo method is reserved for internal use only.
old-location : wdf\wdfgettriageinfo.htm
old-project : wdf
ms.assetid : F6B1DC49-B691-45E4-8DE9-ADCD73D90ADE
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : WdfGetTriageInfo
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdfverifier.h
req.include-header : Wdf.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 1.11
req.umdf-ver : 2.0
req.alt-api : WdfGetTriageInfo
req.alt-loc : Wdfverifier.h
req.ddi-compliance : DriverCreate
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : "*PWDF_USB_REQUEST_COMPLETION_PARAMS, WDF_USB_REQUEST_COMPLETION_PARAMS"
req.product : Windows 10 or later.
---


# WdfGetTriageInfo function
<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WdfGetTriageInfo</b> method is reserved for internal use only.

## Syntax

````
PVOID WdfGetTriageInfo(void);
````

## Parameters

This function has no parameters.

## Return Value

None


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** | 1.11 |
| **Minimum UMDF version** | 2.0 |
| **Header** | wdfverifier.h (include Wdf.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** | DriverCreate |