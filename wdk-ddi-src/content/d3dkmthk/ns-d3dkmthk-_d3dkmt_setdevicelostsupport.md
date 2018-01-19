---
UID : NS:d3dkmthk._D3DKMT_SETDEVICELOSTSUPPORT
title : _D3DKMT_SETDEVICELOSTSUPPORT
author : windows-driver-content
description : Used to indicate whether a device can recover from losing a graphics device.
old-location : display\d3dkmt-setdevicelostsupport.htm
old-project : display
ms.assetid : 191ea8ac-6646-44db-88eb-54dc51afef17
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _D3DKMT_SETDEVICELOSTSUPPORT, D3DKMT_SETDEVICELOSTSUPPORT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmthk.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3DKMT_SETDEVICELOSTSUPPORT
req.alt-loc : d3dkmthk.h
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
req.typenames : D3DKMT_SETDEVICELOSTSUPPORT
---

# _D3DKMT_SETDEVICELOSTSUPPORT structure
Used to indicate whether a device can recover from losing a graphics device.

## Syntax
````
typedef struct _D3DKMT_SETDEVICELOSTSUPPORT {
  D3DKMT_HANDLE hDevice;
  BOOLEAN       Support;
} D3DKMT_SETDEVICELOSTSUPPORT;
````

## Members

        
            `hDevice`

            A handle to the device.
        
            `Support`

            Indicates whether or not the device can recover from losing the graphics device.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmthk.h |