---
UID : NN:wudfddi.IWDFPropertyStoreFactory
title : IWDFPropertyStoreFactory
author : windows-driver-content
description : The IWDFPropertyStoreFactory interface is a factory interface that is used to create a property store interface.
old-location : wdf\iwdfpropertystorefactory.htm
old-project : wdf
ms.assetid : 41d77cf1-6f85-4f43-b2d8-1da4c9dac380
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : IWDFWorkItem, IWDFWorkItem::GetParentObject, GetParentObject
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : wudfddi.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 1.9
req.alt-api : IWDFPropertyStoreFactory
req.alt-loc : WUDFx.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : Unavailable in UMDF 2.0 and later.
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : WUDFx.dll
req.irql : 
req.typenames : "*PPOWER_ACTION, POWER_ACTION"
req.product : Windows 10 or later.
---

# IWDFPropertyStoreFactory interface

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>IWDFPropertyStoreFactory</b> interface is a factory interface that is used to create a property store interface.

## Methods

<p>The <b>IWDFPropertyStoreFactory</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [wudfddi.IWDFPropertyStoreFactory.RetrieveDevicePropertyStore](nf-wudfddi-iwdfpropertystorefactory-retrievedevicepropertystore.md) | The RetrieveDevicePropertyStore method retrieves a property store interface that drivers can use to access the registry. |

## Remarks

Drivers obtain the <b>IWDFPropertyStoreFactory</b> interface by calling <b>IWDFDevice::QueryInterface</b>,  <b>IWDFDeviceInitialize::QueryInterface</b> or <b>IWDFDeviceInitialize2::QueryInterface</b>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum UMDF version** | 1.9 |
| **Header** | wudfddi.h |
| **DLL** | WUDFx.dll |