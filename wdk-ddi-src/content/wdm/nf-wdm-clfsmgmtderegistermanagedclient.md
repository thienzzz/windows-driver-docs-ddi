---
UID : NF:wdm.ClfsMgmtDeregisterManagedClient
title : ClfsMgmtDeregisterManagedClient function
author : windows-driver-content
description : The ClfsMgmtDeregisterManagedClient routine removes the connection between a client and a log, so that the client no longer manages the log.
old-location : kernel\clfsmgmtderegistermanagedclient.htm
old-project : kernel
ms.assetid : 5dee3b70-9c8d-420d-86f9-9795b4d8b1e8
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : ClfsMgmtDeregisterManagedClient
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Server 2003 R2, Windows Vista, and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ClfsMgmtDeregisterManagedClient
req.alt-loc : Clfs.sys,Ext-MS-Win-fs-clfs-l1-1-0.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Clfs.lib
req.dll : Clfs.sys
req.irql : <= APC_LEVEL
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# ClfsMgmtDeregisterManagedClient function
The <b>ClfsMgmtDeregisterManagedClient</b> routine removes the connection between a client and a log, so that the client no longer manages the log.

## Syntax

````
NTSTATUS ClfsMgmtDeregisterManagedClient(
  _In_ CLFS_MGMT_CLIENT Client
);
````

## Parameters

`ClientCookie`




## Return Value

The <b>ClfsMgmtDeregisterManagedClient</b> routine returns one of the following NTSTATUS values:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The client is no longer associated with the log.
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>CLFS management was not able to deregister the client.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>A <b>NULL</b> value was supplied for the <i>Client</i> parameter.
<dl>
<dt><b>STATUS_INVALID_PARAMETER_1</b></dt>
</dl>The value that  was supplied for the <i>Client</i> parameter does not represent a valid client.

## Remarks

After calling the <b>ClfsMgmtDeregisterManagedClient</b> routine, a client's callback functions will no longer be invoked.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-clfsmgmtregistermanagedclient.md">ClfsMgmtRegisterManagedClient</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ClfsMgmtDeregisterManagedClient routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>