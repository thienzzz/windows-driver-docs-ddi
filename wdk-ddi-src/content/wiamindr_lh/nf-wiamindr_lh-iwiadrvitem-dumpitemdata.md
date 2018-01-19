---
UID : NF:wiamindr_lh.IWiaDrvItem.DumpItemData
title : IWiaDrvItem::DumpItemData method
author : windows-driver-content
description : The IWiaDrvItem::DumpItemData method dumps private data associated with an IWiaDrvItem item into an allocated private buffer.
old-location : image\iwiadrvitem_dumpitemdata.htm
old-project : image
ms.assetid : e17da654-60a7-4942-99f9-f55df87a1ca3
ms.author : windowsdriverdev
ms.date : 1/17/2018
ms.keywords : IWiaDrvItem, IWiaDrvItem::DumpItemData, DumpItemData
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : wiamindr_lh.h
req.include-header : Wiamindr.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IWiaDrvItem.DumpItemData
req.alt-loc : wiamindr_lh.h
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
req.typenames : "*PSCANWINDOW, SCANWINDOW"
req.product : Windows 10 or later.
---


# DumpItemData method
The <b>IWiaDrvItem::DumpItemData</b> method dumps private data associated with an <b>IWiaDrvItem</b> item into an allocated private buffer.

## Syntax

````
HRESULT DumpItemData(
  [out, optional] BSTR *bstrDrvItemData
);
````

## Parameters

`__MIDL__IWiaDrvItem0015`




## Return Value

If the method succeeds, it returns S_OK. If the method fails the buffer allocation, it returns E_OUTOFMEMORY. If the method fails for another reason, it returns a standard COM error code.

## Remarks

This method is provided for Microsoft internal debugging only. It will return E_NOTIMPL on the release operating system. </p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wiamindr_lh.h (include Wiamindr.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |