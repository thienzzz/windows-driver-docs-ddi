---
UID : NS:dispmprt._DXGK_CHILD_CONTAINER_ID
title : _DXGK_CHILD_CONTAINER_ID
author : windows-driver-content
description : Contains the container ID for a child device that is connected to a display adapter.
old-location : display\dxgk_child_container_id.htm
old-project : display
ms.assetid : 9573f6e9-80a6-4390-b2ab-4543e3b1f5f4
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_CHILD_CONTAINER_ID, *PDXGK_CHILD_CONTAINER_ID, DXGK_CHILD_CONTAINER_ID
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : dispmprt.h
req.include-header : Dispmprt.h
req.target-type : Windows
req.target-min-winverclnt : Windows 8
req.target-min-winversvr : Windows Server 2012
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_CHILD_CONTAINER_ID
req.alt-loc : Dispmprt.h
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
req.typenames : "*PDXGK_CHILD_CONTAINER_ID, DXGK_CHILD_CONTAINER_ID"
---

# _DXGK_CHILD_CONTAINER_ID structure
Contains the container ID for a child device that is connected to a display adapter.

## Syntax
````
typedef struct _DXGK_CHILD_CONTAINER_ID {
  GUID ContainerId;
  struct {
    ULONG64 PortId;
    USHORT  ManufacturerName;
    USHORT  ProductCode;
  } EldInfo;
} DXGK_CHILD_CONTAINER_ID, *PDXGK_CHILD_CONTAINER_ID;
````

## Members

        
            `ContainerId`

            The container ID for the child device. For more information, see the Remarks section.
        
            `EldInfo`

            This structure contains the information that the operating system used to generate the container ID for the child device.

    ## Remarks
        The operating system calls the display miniport driver's <a href="..\dispmprt\nc-dispmprt-dxgkddi_query_child_relations.md">DxgkDdiQueryChildRelations</a> function to enumerate the child devices of the display adapter. The operating system then calls the display miniport driver's <a href="..\dispmprt\nc-dispmprt-dxgkddi_query_device_descriptor.md">DxgkDdiQueryDeviceDescriptor</a> function for each child device to obtain the  Extended Display Information Data (EDID) for the device. For more information on this procedure, see <a href="https://msdn.microsoft.com/3bec2117-aef4-41fc-b88a-0081c7c9fe3d">Enumerating Child Devices of a Display Adapter</a>.

Based on the device's EDID data, the operating system generates a default container ID for the child device. Then, the operating system calls the display miniport driver's <a href="..\dispmprt\nc-dispmprt-dxgkddi_get_child_container_id.md">DxgkDdiGetChildContainerId</a> function and passes a pointer to a <b>DXGK_CHILD_CONTAINER_ID</b> structure through the <i>ContainerId</i> parameter. The <b>ContainerId</b> member of this structure contains the default container ID for the child display device.

The display miniport driver can either accept the default container ID because the display hardware has no container ID coded into the firmware, or it can set the <b>ContainerId</b> member to a unique identifier obtained from the display hardware device before it returns from the call to <a href="..\dispmprt\nc-dispmprt-dxgkddi_get_child_container_id.md">DxgkDdiGetChildContainerId</a>.

For more information about Container IDs, see <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/dd542646">Container IDs</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dispmprt.h (include Dispmprt.h) |

    ## See Also

        <dl>
<dt>
<a href="..\dispmprt\nc-dispmprt-dxgkddi_get_child_container_id.md">DxgkDdiGetChildContainerId</a>
</dt>
<dt>
<a href="..\dispmprt\nc-dispmprt-dxgkddi_query_child_relations.md">DxgkDdiQueryChildRelations</a>
</dt>
<dt>
<a href="..\dispmprt\nc-dispmprt-dxgkddi_query_device_descriptor.md">DxgkDdiQueryDeviceDescriptor</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGK_CHILD_CONTAINER_ID structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>