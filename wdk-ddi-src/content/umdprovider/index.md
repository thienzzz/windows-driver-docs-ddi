---
UID : NA:umdprovider
ms.assetid : 63774c7c-5cbd-360a-a843-0f6012d66a41
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# umdprovider.h header



umdprovider.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [UMDEtwLogMapAllocation](nf-umdprovider-umdetwlogmapallocation.md) | Describes how a Microsoft DirectX graphics kernel subsystem (Dxgkrnl.sys) memory allocation, or a portion of the allocation, is being used. |
| [UMDEtwLogUnmapAllocation](nf-umdprovider-umdetwlogunmapallocation.md) | Indicates that a Microsoft DirectX graphics kernel subsystem (Dxgkrnl.sys) memory allocation, or a portion of the allocation, is no longer being used. Call this function whether or not the allocation is being destroyed. |
| [UMDEtwRegister](nf-umdprovider-umdetwregister.md) | Registers the event trace provider. The driver should call this function before it makes any calls to log events. |
| [UMDEtwUnregister](nf-umdprovider-umdetwunregister.md) | Unregisters the event trace provider. Call this function before the user-mode driver is unloaded. After this function is called, the driver should not make any other calls to log events. |



## Structures
| Title | Description |
| ---- |:---- |
| [_UMDETW_ALLOCATION_USAGE](ns-umdprovider-_umdetw_allocation_usage.md) | Indicates the reason for mapping from a Microsoft Direct3D memory allocation to a Microsoft DirectX graphics kernel subsystem (Dxgkrnl.sys) allocation. |


## Enumerations
| Title | Description |
| ---- |:---- |
| [_UMDETW_ALLOCATION_SEMANTIC](ne-umdprovider-_umdetw_allocation_semantic.md) | Indicates what a memory allocation is used for if the allocation is internal to the user-mode driver. |