---
UID : NF:vmbuskernelmodeclientlibapi.VmbChannelSaveContinue
title : VmbChannelSaveContinue function
author : windows-driver-content
description : The VmbChannelSaveContinue function saves the channel state to a buffer. Run the VmbChannelSaveBegin before you run this function. The driver must check the return value of the function.
old-location : netvista\vmbchannelsavecontinue.htm
old-project : netvista
ms.assetid : 57266CAE-C069-4379-92FD-0F93FECC6EB5
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : VmbChannelSaveContinue
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : vmbuskernelmodeclientlibapi.h
req.include-header : VmbusKernelModeClientLibApi.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 1.13
req.umdf-ver : 2.0
req.alt-api : VmbChannelSaveContinue
req.alt-loc : VmbusKernelModeClientLibApi.h
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
req.typenames : "*PVIDEO_PORT_AGP_SERVICES, VIDEO_PORT_AGP_SERVICES"
req.product : Windows 10 or later.
---


# VmbChannelSaveContinue function
<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>VmbChannelSaveContinue</b> function saves the channel state to a buffer.  Run the <a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbchannelsavebegin.md">VmbChannelSaveBegin</a> before you run this function. The driver must check the return value of the function.

## Syntax

````
NTSTATUS VmbChannelSaveContinue(
  _In_  VMBCHANNEL                                                       Channel,
  _Out_ writes_bytes_to_(SaveBufferSize, *BytesFilled)
            PVOID SaveBuffer,
  _In_  ULONG                                                            SaveBufferSize,
  _Out_ PULONG                                                           BytesFilled,
  _Out_ PULONG                                                           BytesRequired
);
````

## Parameters

`Channel`

A handle for a channel to save.

`SaveBuffer`

A pointer to buffer into which to save state information.

`SaveBufferSize`

The size, in bytes, of the save buffer.

`BytesFilled`

A pointer to a variable that receives the number of bytes
that were copied to the save buffer.

`BytesRequired`

A pointer to a variable that receives the number of
bytes that are needed for this function to make progress on the next
call.


## Return Value

<b>VmbChannelSaveContinue</b> returns the following values: 
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The state was saved.
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL </b></dt>
</dl>The save buffer was too small.  The <i>BytesNeeded</i>
parameter     contains the number of bytes that are required to make any progress.

<dl>
<dt><b>STATUS_STATUS_BUFFER_OVERFLOW</b></dt>
</dl>Some data was written to the save
buffer, but there is more data to be saved.

## Remarks

The save process saves
the data in "chunks" and can continue from the point it stopped. 

If the caller did not allocate enough space in advance, multiple calls may be needed.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** | 1.13 |
| **Minimum UMDF version** | 2.0 |
| **Header** | vmbuskernelmodeclientlibapi.h (include VmbusKernelModeClientLibApi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\vmbuskernelmodeclientlibapi\nf-vmbuskernelmodeclientlibapi-vmbchannelsavebegin.md">VmbChannelSaveBegin</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20VmbChannelSaveContinue function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>