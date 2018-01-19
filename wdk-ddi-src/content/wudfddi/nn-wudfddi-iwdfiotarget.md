---
UID : NN:wudfddi.IWDFIoTarget
title : IWDFIoTarget
author : windows-driver-content
description : The IWDFIoTarget interface exposes the I/O target object that typically represents a lower driver in the stack.
old-location : wdf\iwdfiotarget.htm
old-project : wdf
ms.assetid : bebe79c8-28d1-4976-b314-b73e6e9b7b9c
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
req.umdf-ver : 1.5
req.alt-api : IWDFIoTarget
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

# IWDFIoTarget interface

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>IWDFIoTarget</b> interface exposes the I/O target object that typically represents a lower driver in the stack.

## Methods

<p>The <b>IWDFIoTarget</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [wudfddi.IWDFIoTarget.CancelSentRequestsForFile](nf-wudfddi-iwdfiotarget-cancelsentrequestsforfile.md) | The CancelSentRequestsForFile method cancels all I/O requests that have been sent on behalf of the specified file object. |
| [wudfddi.IWDFIoTarget.FormatRequestForIoctl](nf-wudfddi-iwdfiotarget-formatrequestforioctl.md) | The FormatRequestForIoctl method formats an I/O request object for an I/O control operation. |
| [wudfddi.IWDFIoTarget.FormatRequestForRead](nf-wudfddi-iwdfiotarget-formatrequestforread.md) | The FormatRequestForRead method formats an I/O request object for a read operation. |
| [wudfddi.IWDFIoTarget.FormatRequestForWrite](nf-wudfddi-iwdfiotarget-formatrequestforwrite.md) | The FormatRequestForWrite method formats an I/O request object for a write operation. |
| [wudfddi.IWDFIoTarget.GetTargetFile](nf-wudfddi-iwdfiotarget-gettargetfile.md) | The GetTargetFile method retrieves the framework file object that is associated with the I/O target object. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum UMDF version** | 1.5 |
| **Header** | wudfddi.h |
| **DLL** | WUDFx.dll |