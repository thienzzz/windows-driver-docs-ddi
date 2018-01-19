---
UID : NC:hdaudio.PREGISTER_NOTIFICATION_EVENT
title : PREGISTER_NOTIFICATION_EVENT
author : windows-driver-content
description : The RegisterNotificationEvent routine registers a kernel event so that it can receive DMA progress notifications.The function pointer type for a RegisterNotificationEvent routine is defined as follows.
old-location : audio\registernotificationevent.htm
old-project : audio
ms.assetid : 44702d79-80ac-411f-ae47-bf60b9cb541d
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _SM_SetRNIDMgmtInfo_OUT, SM_SetRNIDMgmtInfo_OUT, *PSM_SetRNIDMgmtInfo_OUT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : hdaudio.h
req.include-header : Hdaudio.h
req.target-type : Desktop
req.target-min-winverclnt : Available in Windows Vista and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RegisterNotificationEvent
req.alt-loc : Hdaudio.h
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
req.typenames : SM_SetRNIDMgmtInfo_OUT, *PSM_SetRNIDMgmtInfo_OUT
---


# PREGISTER_NOTIFICATION_EVENT callback function
The <i>RegisterNotificationEvent</i> routine registers a kernel event so that it can receive DMA progress notifications.

The function pointer type for a <i>RegisterNotificationEvent</i> routine is defined as follows.

## Syntax

```
PREGISTER_NOTIFICATION_EVENT PregisterNotificationEvent;

NTSTATUS PregisterNotificationEvent(
  PVOID _context,
  HANDLE Handle,
  PKEVENT NotificationEvent
)
{...}
```

## Parameters

`_context`



`Handle`



`NotificationEvent`




## Return Value

<i>RegisterNotificationEvent</i> returns STATUS_SUCCESS if the call successfully registers the event. Otherwise, the routine returns STATUS_INSUFFICIENT_RESOURCES to indicate that there are insufficient resources that are available to complete the operation.

## Remarks

<i>RegisterNotificationEvent</i> registers a kernel event with the HD Audio bus driver.  The HD Audio bus driver maintains a list of registered notification events for each DMA engine, and signals them every time that the engine receives an IOC interrupt.  Events are unregistered by using <a href="..\hdaudio\nc-hdaudio-punregister_notification_event.md">UnregisterNotificationEvent</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hdaudio.h (include Hdaudio.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\hdaudio\nc-hdaudio-pallocate_capture_dma_engine.md">AllocateCaptureDmaEngine</a>
</dt>
<dt>
<a href="..\hdaudio\nc-hdaudio-pallocate_dma_buffer_with_notification.md">AllocateDmaBufferWithNotification</a>
</dt>
<dt>
<a href="..\hdaudio\nc-hdaudio-pallocate_render_dma_engine.md">AllocateRenderDmaEngine</a>
</dt>
<dt>
<a href="..\hdaudio\ns-hdaudio-_hdaudio_bus_interface_v2.md">HDAUDIO_BUS_INTERFACE_V2</a>
</dt>
<dt>
<a href="..\hdaudio\nc-hdaudio-punregister_notification_event.md">UnregisterNotificationEvent</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20PREGISTER_NOTIFICATION_EVENT callback function%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>