---
UID : NF:sensorsclassextension.ISensorClassExtension.Uninitialize
title : ISensorClassExtension::Uninitialize method
author : windows-driver-content
description : The ISensorClassExtension::Uninitialize method uninitializes the sensor class extension object.
old-location : sensors\isensorclassextension_uninitialize.htm
old-project : sensors
ms.assetid : 204a6126-bb69-4a96-acbf-3ad5b8ae0f04
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : ISensorClassExtension, ISensorClassExtension::Uninitialize, Uninitialize
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : sensorsclassextension.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : Uninitialize
req.alt-loc : SensorsClassExtension.lib,SensorsClassExtension.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : SensorsClassExtension.lib
req.dll : 
req.irql : 
req.typenames : SensorConnectionType
req.product : Windows 10 or later.
---


# Uninitialize method
The <a href="https://msdn.microsoft.com/library/windows/hardware/ff545547">ISensorClassExtension::Uninitialize</a> method uninitializes the sensor class extension object.

## Syntax

````
HRESULT Uninitialize();
````

## Parameters

This function has no parameters.

## Return Value

This method returns an HRESULT. Possible values include, but are not limited to, one of the following values.
<dl>
<dt><b>S_OK</b></dt>
</dl>The method succeeded.
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CAN_NOT_COMPLETE)</b></dt>
</dl>The class extension is not initialized.

 

This method returns an HRESULT. Possible values include, but are not limited to, one of the following values.
<dl>
<dt><b>S_OK</b></dt>
</dl>The method succeeded.
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CAN_NOT_COMPLETE)</b></dt>
</dl>The class extension is not initialized.

 

This method returns an HRESULT. Possible values include, but are not limited to, one of the following values.
<dl>
<dt><b>S_OK</b></dt>
</dl>The method succeeded.
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_CAN_NOT_COMPLETE)</b></dt>
</dl>The class extension is not initialized.

## Remarks

Typically, you will uninitialize  the sensor class extension when the driver is unloading. We recommend that you perform uninitialization steps when called by UMDF in <a href="https://msdn.microsoft.com/library/windows/hardware/ff556768">IPnpCallbackHardware::OnReleaseHardware</a>.

If you must, for some reason, otherwise release and uninitialize the sensor class extension, you must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff558954">IWDFIoQueue::DrainSynchronously</a> before calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff545547">ISensorClassExtension::Uninitialize</a>. You can retrieve the queue interface by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff558830">IWDFDevice::GetDefaultIoQueue</a> on the WDF device object. Then, call <b>IWDFIoQueue::DrainSynchronously</b> to process all the queued requests. Calling <b>IWDFIoQueue::DrainSynchronously</b> blocks the queuing of new requests, so you must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff558977">IWDFIoQueue::Start</a> after you reinitialize the class extension.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | sensorsclassextension.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |