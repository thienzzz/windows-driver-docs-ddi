---
UID : NF:extsfns.IDebugFailureAnalysis2.AddBuffer
title : IDebugFailureAnalysis2::AddBuffer method
author : windows-driver-content
description : The AddBuffer method adds a new FA entry to a DebugFailureAnalysis object, and writes the bytes from a specified buffer to the data block of the new FA entry.
old-location : debugger\idebugfailureanalysis2_addbuffer.htm
old-project : debugger
ms.assetid : E6510000-E390-4631-9D47-5A57AB845EF6
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugFailureAnalysis2, IDebugFailureAnalysis2::AddBuffer, AddBuffer
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : extsfns.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugFailureAnalysis2.AddBuffer
req.alt-loc : extsfns.h
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
req.typenames : FA_EXTENSION_PLUGIN_PHASE
---


# AddBuffer method
The <b>AddBuffer</b> method adds a new <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a> to a <a href="..\extsfns\nn-extsfns-idebugfailureanalysis2.md">DebugFailureAnalysis</a> object, and writes the bytes from a specified buffer to the data block of the new FA entry.

## Syntax

````
FA_ENTRY AddBuffer(
       FA_TAG        Tag,
  [in] FA_ENTRY_TYPE EntryType,
  [in] PVOID         Buf,
  [in] ULONG         Size
);
````

## Parameters

`Tag`

A value in the <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/writing-an-analysis-extension-to-extend--analyze">FA_TAG</a> enumeration.

`EntryType`

A value in the <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/debugger/writing-an-analysis-extension-to-extend--analyze">FA_ENTRY_TYPE</a> enumeration. This parameter specifies the data type of the data in <i>Buf</i>.

`Buf`

A pointer to a buffer that contains the bytes to be written to the data block of the new <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a>.

`Size`

The size, in bytes, of the buffer pointed to by <i>Buf</i>.


## Return Value

If this method succeeds, it returns a pointer to the new <a href="..\extsfns\ns-extsfns-_fa_entry.md">FA_ENTRY</a> structure. Otherwise, it returns <b>NULL</b>.

## Remarks

This method creates a new <a href="https://msdn.microsoft.com/759DE159-F2A8-4BB1-AAF5-B2B91C4F91B0">FA entry</a> with the tag specified by <i>Tag</i>, and it associates the tag with the data type specified by <i>EntryType</i>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | extsfns.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\extsfns\nn-extsfns-idebugfailureanalysis2.md">IDebugFailureAnalysis2</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/7648F789-85D5-4247-90DD-2EAA43543483">Writing an Analysis Extension Plug-in to Extend !analyze</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983423">SetBuffer</a>
</dt>
<dt>
<a href="..\extsfns\nc-extsfns-ext_analysis_plugin.md">_EFN_Analyze</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugFailureAnalysis2::AddBuffer method%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>