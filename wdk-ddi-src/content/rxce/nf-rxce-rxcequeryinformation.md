---
UID : NF:rxce.RxCeQueryInformation
title : RxCeQueryInformation function
author : windows-driver-content
description : RxCeQueryInformation queries information about a connection in a caller-allocated buffer.
old-location : ifsk\rxcequeryinformation.htm
old-project : ifsk
ms.assetid : 58dd579c-3fb8-45c7-a7bc-ca0919166153
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RxCeQueryInformation
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : rxce.h
req.include-header : Rxce.h, Rxcehdlr.h, Tdi.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RxCeQueryInformation
req.alt-loc : rxce.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= APC_LEVEL
req.typenames : "*LPRILWRITEPHONEBOOKENTRYPARAMS, RILWRITEPHONEBOOKENTRYPARAMS"
req.product : Windows 10 or later.
---


# RxCeQueryInformation function
<b>RxCeQueryInformation</b> queries information about a connection in a caller-allocated buffer.

## Syntax

````
NTSTATUS RxCeQueryInformation(
  _In_  PRXCE_VC                          pVc,
  _In_  RXCE_CONNECTION_INFORMATION_CLASS InformationClass,
  _Out_ PVOID                             pInformation,
  _In_  ULONG                             Length
);
````

## Parameters

`pVc`

A pointer to the virtual circuit associated with this connection.

`InformationClass`

The desired information class for this query type. The value specified for <i>InformationClass</i> determines the type of information that is returned. This parameter is an enumeration defined in <i>rxcehdlr.h</i> and can be one of the following values:

`pInformation`

The caller-supplied buffer for returning information.

`Length`

The length of  the buffer.


## Return Value

<b>RxCeQueryInformation</b> returns STATUS_SUCCESS on success or one of the following warning or error codes: 
<dl>
<dt><b>STATUS_BUFFER_OVERFLOW</b></dt>
</dl>This specified <i>length</i> of the output buffer pointed to by <i>pInformation</i> was not large enough to receive the information requested by the <i>InformationClass</i> query type.
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>The allocation of nonpaged pool memory needed by this routine failed. 
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>This value can be returned for any of the following conditions:
<dl>
<dd>
The <i>pVC</i> parameter passed to this routine was invalid.

</dd>
<dd>
The connection, address, or transport defined for this virtual circuit was invalid. 

</dd>
<dd>
The <i>InformationClass</i> for this query type was not one of the allowed values.

</dd>
</dl>The <i>pVC</i> parameter passed to this routine was invalid.

The connection, address, or transport defined for this virtual circuit was invalid. 

The <i>InformationClass</i> for this query type was not one of the allowed values.

## Remarks

<b>RxCeQueryInformation</b> returns information for a given virtual circuit. The  only values for <i>InformationClass</i> that can be specified when calling <b>RxCeQueryInformation</b> are the following:

RxCeTransportProviderInformation

RxCeConnectionInformation

RxCeConnectionEndpointInformation

RxCeRemoteAddressInformation

For some values of <i>InformationClass</i>, <b>RxCeQueryInformation</b> calls <b>TdiBuildQueryInformation</b> and TDI to retrieve the requested information.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rxce.h (include Rxce.h, Rxcehdlr.h, Tdi.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\rxce\nf-rxce-rxcequeryadapterstatus.md">RxCeQueryAdapterStatus</a>
</dt>
<dt>
<a href="..\rxce\nf-rxce-rxcequerytransportinformation.md">RxCeQueryTransportInformation</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RxCeQueryInformation function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>