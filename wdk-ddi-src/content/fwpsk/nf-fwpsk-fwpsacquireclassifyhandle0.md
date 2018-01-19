---
UID : NF:fwpsk.FwpsAcquireClassifyHandle0
title : FwpsAcquireClassifyHandle0 function
author : windows-driver-content
description : The FwpsAcquireClassifyHandle0 function generates a classification handle that is used to identify asynchronous classification operations and requests for writable layer data.Note  FwpsAcquireClassifyHandle0 is a specific version of FwpsAcquireClassifyHandle. See WFP Version-Independent Names and Targeting Specific Versions of Windows for more information.
old-location : netvista\fwpsacquireclassifyhandle0.htm
old-project : netvista
ms.assetid : 7348d937-6541-47a7-ae70-7d851d41bc1a
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FwpsAcquireClassifyHandle0
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 7.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FwpsAcquireClassifyHandle0
req.alt-loc : fwpkclnt.lib,fwpkclnt.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Fwpkclnt.lib
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : FWPS_VSWITCH_EVENT_TYPE
---


# FwpsAcquireClassifyHandle0 function
The 
  <b>FwpsAcquireClassifyHandle0</b> function generates a classification handle that is used to identify
  asynchronous classification operations and requests for writable layer data.

## Syntax

````
NTSTATUS NTAPI FwpsAcquireClassifyHandle0(
  _In_  void   *classifyContext,
  _In_  UINT32 flags,
  _Out_ UINT64 *classifyHandle
);
````

## Parameters

`classifyContext`

The 
     <i>classifyContext</i> parameter from 
     <a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn1.md">classifyFn1</a>. The WFP engine passes this
     value to the callout driver's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>.

`flags`

Reserved for future use. Set to 0.

`classifyHandle`

A pointer to a variable that receives a classification handle. This handle is needed by subsequent
     function calls as noted in Remarks.


## Return Value

The 
     <b>FwpsAcquireClassifyHandle0</b> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>A handle to the classify request was successfully returned. The variable that the 
       <i>classifyHandle</i> parameter points to contains the handle for the classify request.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

<b>FwpsAcquireClassifyHandle0</b> is a support function for asynchronous classification and data
    modification. The handle returned by this function is required as a parameter for the following
    functions:


<a href="..\fwpsk\nf-fwpsk-fwpspendclassify0.md">FwpsPendClassify0</a>



<a href="..\fwpsk\nf-fwpsk-fwpsacquirewritablelayerdatapointer0.md">
       FwpsAcquireWritableLayerDataPointer0</a>



<a href="..\fwpsk\nf-fwpsk-fwpsapplymodifiedlayerdata0.md">
       FwpsApplyModifiedLayerData0</a>



<a href="..\fwpsk\nf-fwpsk-fwpscompleteclassify0.md">FwpsCompleteClassify0</a>



<a href="..\fwpsk\nf-fwpsk-fwpsreleaseclassifyhandle0.md">FwpsReleaseClassifyHandle0</a>


For each call to this function, the callout driver must call 
    <a href="..\fwpsk\nf-fwpsk-fwpsreleaseclassifyhandle0.md">FwpsReleaseClassifyHandle0</a> to
    free the system resources associated with the handle.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
</dt>
<dt>
<a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn1.md">classifyFn1</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpscompleteclassify0.md">FwpsCompleteClassify0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpspendclassify0.md">FwpsPendClassify0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpsreleaseclassifyhandle0.md">FwpsReleaseClassifyHandle0</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FwpsAcquireClassifyHandle0 function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>