---
UID : NC:bthddi.PFNBTH_IS_BLUETOOTH_VERSION_AVAILABLE
title : PFNBTH_IS_BLUETOOTH_VERSION_AVAILABLE
author : windows-driver-content
description : The IsBluetoothVersionAvailable function checks whether a given Bluetooth version is supported by the operating system.
old-location : bltooth\isbluetoothversionavailable.htm
old-project : bltooth
ms.assetid : 10662237-18b4-4f37-a704-985b2db0d689
ms.author : windowsdriverdev
ms.date : 12/21/2017
ms.keywords : IBidiSpl2, IBidiSpl2::UnbindDevice, UnbindDevice
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : bthddi.h
req.include-header : Bthddi.h
req.target-type : Desktop
req.target-min-winverclnt : Versions: Supported in Windows Vista, and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IsBluetoothVersionAvailable
req.alt-loc : bthddi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE
---


# PFNBTH_IS_BLUETOOTH_VERSION_AVAILABLE callback function
The 
  <i>IsBluetoothVersionAvailable</i> function checks whether a given Bluetooth version is supported by the
  operating system.

## Syntax

```
PFNBTH_IS_BLUETOOTH_VERSION_AVAILABLE PfnbthIsBluetoothVersionAvailable;

BOOLEAN PfnbthIsBluetoothVersionAvailable(
  UCHAR MajorVersion,
  UCHAR MinorVersion
)
{...}
```

## Parameters

`MajorVersion`

This parameter specifies the major version number of Bluetooth that is requested.

`MinorVersion`

This parameter specifies the minor version number of Bluetooth that is requested.


## Return Value

<i>IsBluetoothVersionAvailable</i> returns <b>TRUE</b> if the Bluetooth version that the operating system
     provides is greater than or equal to the Bluetooth version number that is being requested.

## Remarks

Bluetooth profile drivers should call this function before performing any operations that are not
    supported in all Bluetooth versions.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | bthddi.h (include Bthddi.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |