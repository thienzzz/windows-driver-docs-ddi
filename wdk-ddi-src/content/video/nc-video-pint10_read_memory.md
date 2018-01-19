---
UID : NC:video.PINT10_READ_MEMORY
title : PINT10_READ_MEMORY
author : windows-driver-content
description : The Int10ReadMemory function reads a block of memory in the context of another thread and stores it in an output buffer.
old-location : display\int10readmemory.htm
old-project : display
ms.assetid : 94b72ad0-1ace-4fde-a4a9-1078103e3d9b
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _VHF_CONFIG, VHF_CONFIG, *PVHF_CONFIG
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : video.h
req.include-header : Video.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : Int10ReadMemory
req.alt-loc : video.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : VHF_CONFIG, *PVHF_CONFIG
req.product : Windows 10 or later.
---


# PINT10_READ_MEMORY callback function
The <i>Int10ReadMemory </i>function reads a block of memory in the context of another thread and stores it in an output buffer.

## Syntax

```
PINT10_READ_MEMORY Pint10ReadMemory;

VP_STATUS Pint10ReadMemory(
  IN PVOID Context,
  IN USHORT Seg,
  IN USHORT Off,
  OUT PVOID Buffer,
  IN ULONG Length
)
{...}
```

## Parameters

`Context`

Pointer to a video port driver-defined context for the interface. This should be the same as the value in the <b>Context</b> member of the <a href="..\video\ns-video-_video_port_int10_interface.md">VIDEO_PORT_INT10_INTERFACE</a> structure after <a href="..\video\nf-video-videoportqueryservices.md">VideoPortQueryServices</a> returns.

`Seg`

Specifies the segment address of the buffer to be read.

`Off`

Specifies the offset within the segment indicated by the <i>Seg</i> parameter.

`Buffer`

Pointer to a memory location that indicates the beginning of the output buffer.

`Length`

Is the length, in bytes, of the output buffer specified by the <i>Buffer</i> parameter.


## Return Value

The <i>Int10ReadMemory</i> function returns NO_ERROR upon success. Otherwise it returns an appropriate error code.

## Remarks

The video port implements this function, which can be accessed through a pointer in the <a href="..\video\ns-video-_video_port_int10_interface.md">VIDEO_PORT_INT10_INTERFACE</a> structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | video.h (include Video.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\video\ns-video-_video_port_int10_interface.md">VIDEO_PORT_INT10_INTERFACE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PINT10_READ_MEMORY callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>