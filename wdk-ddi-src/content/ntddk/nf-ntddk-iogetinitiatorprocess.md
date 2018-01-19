---
UID : NF:ntddk.IoGetInitiatorProcess
title : IoGetInitiatorProcess function
author : windows-driver-content
description : The IoGetInitiatorProcess routine retrieves the process which initiated the creation of a file object if different than the process which is issuing the create.
old-location : kernel\iogetinitiatorprocess.htm
old-project : kernel
ms.assetid : 653B4FD5-4C07-420A-BE8A-CC8C46BC6F0F
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : IoGetInitiatorProcess
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoGetInitiatorProcess
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : <= DISPATCH_LEVEL
req.typenames : WHEA_RAW_DATA_FORMAT, *PWHEA_RAW_DATA_FORMAT
---


# IoGetInitiatorProcess function
The IoGetInitiatorProcess routine retrieves the process which initiated the creation of a file object if different than the process which is issuing the create.

## Syntax

````
PEPROCESS WINAPI IoGetInitiatorProcess(
  _In_ PFILE_OBJECT FileObject
);
````

## Parameters

`FileObject`

The file object from which to retrieve the initiator process.


## Return Value

NULL if there is no initiator process. Otherwise, a pointer to which process initiated the creation of the file object.

## Remarks

A driver normally uses IoGetInitiatorProcess to determine which process has issued a request.  However, there are situations where a system component may issue a create on behalf of another process (after a successful create the component will duplicate the handle to the process).  This routine can be used if the driver must know which process the create operation is ultimately intended for. </p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |