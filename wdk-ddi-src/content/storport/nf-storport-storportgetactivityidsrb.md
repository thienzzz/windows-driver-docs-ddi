---
UID : NF:storport.StorPortGetActivityIdSrb
title : StorPortGetActivityIdSrb function
author : windows-driver-content
description : Retrieves the Event Tracing for Windows (ETW) activity ID associated with a request block.
old-location : storage\storportgetactivityidsrb.htm
old-project : storage
ms.assetid : 63E956F5-C87C-45AA-BE16-2AD07F3BA050
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortGetActivityIdSrb
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 8.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortGetActivityIdSrb
req.alt-loc : Storport.lib,Storport.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Storport.lib
req.dll : 
req.irql : Any
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortGetActivityIdSrb function
Retrieves the Event Tracing for Windows (ETW) activity ID associated with a request block.

## Syntax

````
ULONG StorPortGetActivityIdSrb(
  _In_  PVOID               HwDeviceExtension,
  _In_  PSCSI_REQUEST_BLOCK Srb,
  _Out_ LPGUID              ActivityId
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension for the host bus adapter (HBA).

`Srb`

The request block to retrieve the ETW activity ID for.

`ActivityId`

A pointer to a caller-supplied GUID to receive the ETW activity ID.


## Return Value

A status value indicating the result of the notification. This can be one of these values:
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>The ETW activity ID was returned in <i>ActivityId</i>.
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl>The pointer in <i>ActivityId</i> or <i>Srb</i> is NULL.
<dl>
<dt><b>STOR_STATUS_UNSUCCESSFUL</b></dt>
</dl>An ETW activity ID is not associated with the request in <i>Srb</i>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** | Any |
| **DDI compliance rules** |  |