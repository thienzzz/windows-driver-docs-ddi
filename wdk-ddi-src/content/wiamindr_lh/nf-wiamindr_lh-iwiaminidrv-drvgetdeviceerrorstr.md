---
UID : NF:wiamindr_lh.IWiaMiniDrv.drvGetDeviceErrorStr
title : IWiaMiniDrv::drvGetDeviceErrorStr method
author : windows-driver-content
description : The IWiaMiniDrv::drvGetDeviceErrorStr method maps an error code to a Unicode string that describes the error.
old-location : image\iwiaminidrv_drvgetdeviceerrorstr.htm
old-project : image
ms.assetid : c34a6834-8875-400c-9634-6c2b9b68164f
ms.author : windowsdriverdev
ms.date : 1/17/2018
ms.keywords : IWiaMiniDrv, IWiaMiniDrv::drvGetDeviceErrorStr, drvGetDeviceErrorStr
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : wiamindr_lh.h
req.include-header : Wiamindr.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Me and in Windows XP and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IWiaMiniDrv.drvGetDeviceErrorStr
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


# drvGetDeviceErrorStr method
The <b>IWiaMiniDrv::drvGetDeviceErrorStr </b>method maps an error code to a Unicode string that describes the error.

## Syntax

````
HRESULT drvGetDeviceErrorStr(
  [in]            LONG     lFlags,
  [in]            LONG     lDevErrVal,
  [out, optional] LPOLESTR *ppszDevErrStr,
  [out]           LONG     *plDevErr
);
````

## Parameters

`__MIDL__IWiaMiniDrv0039`



`__MIDL__IWiaMiniDrv0040`



`__MIDL__IWiaMiniDrv0041`



`__MIDL__IWiaMiniDrv0042`




## Return Value

On success, the method should return S_OK and clear the device error value pointed to by <i>plDevErr</i>. If the minidriver does not fully implement this method, the method should return E_NOTIMPL. If the minidriver does not recognize the error value passed to this method, the method should return E_INVALIDARG. If the method fails, it should return a standard COM error code and place a minidriver-specific error code value in the memory pointed to by <i>plDevErr</i>.

## Remarks

To obtain an error string that describes a device-specific minidriver-generated error value, the WIA service calls the <b>IWiaMiniDrv::drvGetDeviceErrorStr</b> method. In response to this call, the minidriver should use <b>CoTaskMemAlloc</b> (described in the Microsoft Windows SDK documentation) to allocate memory that will contain a localized Unicode string corresponding to the error code passed to the minidriver. The WIA service (or an application) will free the memory. It is likely that an application will display the string, so it should be meaningful to an end user. The string should be loaded from a resource file, so that it can be localized into a variety of languages.</p>

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