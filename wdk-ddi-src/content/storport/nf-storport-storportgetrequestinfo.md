---
UID : NF:storport.StorPortGetRequestInfo
title : StorPortGetRequestInfo function
author : windows-driver-content
description : The StorPortGetRequestInfo routine retrieves the IO request information associated with a SCSI request block (SRB) and returns it in a STOR_REQUEST_INFO structure.
old-location : storage\storportgetrequestinfo.htm
old-project : storage
ms.assetid : 3B0A25E8-6DBC-4AA9-A0D0-DDB36B402F43
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : StorPortGetRequestInfo
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : storport.h
req.include-header : Storport.h
req.target-type : Universal
req.target-min-winverclnt : Available in Windows 8 and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : StorPortGetRequestInfo
req.alt-loc : storport.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : Any
req.typenames : STOR_SPINLOCK
req.product : Windows 10 or later.
---


# StorPortGetRequestInfo function
The <b>StorPortGetRequestInfo</b> routine retrieves the IO request information associated with a SCSI request block (SRB) and  returns it in a <a href="..\storport\ns-storport-_stor_request_info_v1.md">STOR_REQUEST_INFO</a> structure.

## Syntax

````
ULONG StorPortGetRequestInfo(
  _In_  PVOID               HwDeviceExtension,
  _In_  PSCSI_REQUEST_BLOCK Srb,
  _Out_ PSTOR_REQUEST_INFO  RequestInfo
);
````

## Parameters

`HwDeviceExtension`

A pointer to the hardware device extension for the host bus adapter (HBA).

`Srb`

A pointer to the SRB to be queried.

`RequestInfo`

A pointer to a caller-supplied <a href="..\storport\ns-storport-_stor_request_info_v1.md">STOR_REQUEST_INFO</a> structure.


## Return Value

The <b>StorPortGetRequestInfo</b> routine returns one of these status codes:
<dl>
<dt><b>STOR_STATUS_UNSUPPORTED_VERSION</b></dt>
</dl>The version specified for <a href="..\storport\ns-storport-_stor_request_info_v1.md">STOR_REQUEST_INFO</a> is invalid.
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>The operation was successful.
<dl>
<dt><b>STOR_STATUS_INVALID_PARAMETER</b></dt>
</dl>Either <i>Srb</i> or <i>RequestInfo</i> is set to NULL.

## Remarks

The caller of <b>StorPortGetRequestInfo</b> must set the <b>Version</b> member of <i>RequestInfo</i> to STOR_REQUEST_INFO_VER_1. Otherwise, function will return STOR_STATUS_UNSUPPORTED_VERSION.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | storport.h (include Storport.h) |
| **Library** |  |
| **IRQL** | Any |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\storport\ns-storport-_stor_request_info_v1.md">STOR_REQUEST_INFO</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortGetRequestInfo routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>