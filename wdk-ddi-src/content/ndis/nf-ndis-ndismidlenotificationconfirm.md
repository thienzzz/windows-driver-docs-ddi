---
UID : NF:ndis.NdisMIdleNotificationConfirm
title : NdisMIdleNotificationConfirm function
author : windows-driver-content
description : Miniport drivers call NdisMIdleNotificationConfirm to notify NDIS that the idle network adapter can safely be suspended and transitioned to a low-power state.Miniport drivers call this function during an NDIS selective suspend operation.
old-location : netvista\ndismidlenotificationconfirm.htm
old-project : netvista
ms.assetid : 726B392E-3C7F-4F55-B045-CE022C242F0A
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisMIdleNotificationConfirm
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Universal
req.target-min-winverclnt : Supported in NDIS 6.30 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisMIdleNotificationConfirm
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ndis.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisMIdleNotificationConfirm function
Miniport drivers call <b>NdisMIdleNotificationConfirm</b> to notify NDIS that the idle network adapter can safely be suspended and transitioned to a low-power state.

Miniport drivers call this function during an NDIS selective suspend operation. NDIS begins the operation when it calls the driver's  <a href="..\ndis\nc-ndis-miniport_idle_notification.md">MiniportIdleNotification</a> handler function.



Miniport drivers call <b>NdisMIdleNotificationConfirm</b> to notify NDIS that the idle network adapter can safely be suspended and transitioned to a low-power state.

Miniport drivers call this function during an NDIS selective suspend operation. NDIS begins the operation when it calls the driver's  <a href="..\ndis\nc-ndis-miniport_idle_notification.md">MiniportIdleNotification</a> handler function.

## Syntax

````
VOID NdisMIdleNotificationConfirm(
  _In_ NDIS_HANDLE              MiniportAdapterHandle,
  _In_ NDIS_DEVICE_POWER_STATE  IdlePowerState
);
````

## Parameters

`MiniportAdapterHandle`



`IdlePowerState`




## Return Value

None

## Remarks

Miniport drivers  call <b>NdisMIdleNotificationConfirm</b> after NDIS calls the driver's <a href="..\ndis\nc-ndis-miniport_idle_notification.md">MiniportIdleNotification</a> function. By calling <b>NdisMIdleNotificationConfirm</b>, the driver notifies NDIS that the suspend operation can start and the network adapter can be transitioned to a low-power state. In this call, the miniport driver sets the <i>IdlePowerState</i> parameter to the lowest power state that the device can transition to.

Before the miniport driver calls <b>NdisMIdleNotificationConfirm</b>, it must issue any bus-specific I/O request packets (IRPs) that may be necessary to selectively suspend the network adapter. 

For example, when NDIS calls the <a href="..\ndis\nc-ndis-miniport_idle_notification.md">MiniportIdleNotification</a> function, the USB miniport driver issues the bus-specific I/O request packet (IRP) for a USB idle request (<a href="..\usbioctl\ni-usbioctl-ioctl_internal_usb_submit_idle_notification.md">IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION</a>) to the USB bus driver. When the USB bus driver confirms that the network adapter can transition to a low-power state, it calls the callback routine associated with the IRP. Within the context of the callback routine, the USB miniport driver calls  <b>NdisMIdleNotificationConfirm</b>. For more information, see <a href="https://msdn.microsoft.com/B3F843CD-E9D8-4ABD-9BC9-08C5AB7CDB98">Implementing a USB Idle Request IRP Callback Routine</a>.

For more information about how to handle NDIS selective suspend idle notifications, see <a href="https://msdn.microsoft.com/02D13260-5816-4621-8527-E1E79C9AE975">Handling the NDIS Selective Suspend Idle Notification</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt><b></b></dt>
<dt>
<a href="..\usbioctl\ni-usbioctl-ioctl_internal_usb_submit_idle_notification.md">IOCTL_INTERNAL_USB_SUBMIT_IDLE_NOTIFICATION</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-miniport_idle_notification.md">MiniportIdleNotification</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndismidlenotificationcomplete.md">NdisMIdleNotificationComplete</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisMIdleNotificationConfirm function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>