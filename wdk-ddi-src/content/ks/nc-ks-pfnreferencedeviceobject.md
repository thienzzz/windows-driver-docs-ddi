---
UID : NC:ks.PFNREFERENCEDEVICEOBJECT
title : PFNREFERENCEDEVICEOBJECT
author : windows-driver-content
description : The driver can use this routine to increment the reference count of the PDO.
old-location : stream\kstrreferencedeviceobject.htm
old-project : stream
ms.assetid : f4bf38eb-5028-4fcb-9752-8dab88db5904
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : NpdBrokerUninitialize
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : ks.h
req.include-header : Ks.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KStrReferenceDeviceObject
req.alt-loc : ks.h
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
req.typenames : KEYWORDSELECTOR
---


# PFNREFERENCEDEVICEOBJECT callback function
The driver can use this routine to increment the reference count of the PDO.

## Syntax

```
PFNREFERENCEDEVICEOBJECT Pfnreferencedeviceobject;

void Pfnreferencedeviceobject(
  PVOID Context
)
{...}
```

## Parameters

`Context`

Pointer to a device extension of the device's PDO.


## Return Value

None.

## Remarks

The driver can access this method through the <b>ReferenceDeviceObject</b> member of the <a href="..\ks\ns-ks-bus_interface_reference.md">BUS_INTERFACE_REFERENCE</a> structure.

The device object remains active and enumerated until the reference count returns to 0.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ks.h (include Ks.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |