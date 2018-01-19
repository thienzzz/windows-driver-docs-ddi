---
UID : NA:wudfinterrupt
ms.assetid : cbeea8a1-1f72-3eb6-bde5-b99d677f8a8d
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# wudfinterrupt.h header



wudfinterrupt.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [WUDF_INTERRUPT_DISABLE](nc-wudfinterrupt-wudf_interrupt_disable.md) | A driver's OnInterruptDisable event callback function disables a specified hardware interrupt. |
| [WUDF_INTERRUPT_ENABLE](nc-wudfinterrupt-wudf_interrupt_enable.md) | A driver's OnInterruptEnable event callback function enables a specified hardware interrupt. |
| [WUDF_INTERRUPT_ISR](nc-wudfinterrupt-wudf_interrupt_isr.md) | A driver's OnInterruptIsr event callback function services a hardware interrupt. |
| [WUDF_INTERRUPT_WORKITEM](nc-wudfinterrupt-wudf_interrupt_workitem.md) | A driver's OnInterruptWorkItem event callback function processes interrupt information that the driver's OnInterruptIsr callback function has stored. |
| [WDF_INTERRUPT_EXTENDED_POLICY_INIT](nf-wudfinterrupt-wdf_interrupt_extended_policy_init.md) | The WDF_INTERRUPT_EXTENDED_POLICY_INIT function initializes a WDF_INTERRUPT_EXTENDED_POLICY structure. |
| [WDF_INTERRUPT_INFO_INIT](nf-wudfinterrupt-wdf_interrupt_info_init.md) | The WDF_INTERRUPT_INFO_INIT function initializes a WDF_INTERRUPT_INFO structure. |
| [WUDF_INTERRUPT_CONFIG_INIT](nf-wudfinterrupt-wudf_interrupt_config_init.md) | The WUDF_INTERRUPT_CONFIG_INIT function initializes a WUDF_INTERRUPT_CONFIG structure. |



## Structures
| Title | Description |
| ---- |:---- |
| [_WDF_INTERRUPT_EXTENDED_POLICY](ns-wudfinterrupt-_wdf_interrupt_extended_policy.md) | The WDF_INTERRUPT_EXTENDED_POLICY structure contains information about an interrupt's policy, priority, affinity, and group. |
| [_WDF_INTERRUPT_INFO](ns-wudfinterrupt-_wdf_interrupt_info.md) | The WDF_INTERRUPT_INFO structure contains information about a device's interrupt resource. |
| [_WUDF_INTERRUPT_CONFIG](ns-wudfinterrupt-_wudf_interrupt_config.md) | The WUDF_INTERRUPT_CONFIG structure contains configuration information for a device interrupt. |


## Enumerations
| Title | Description |
| ---- |:---- |
| [_WDF_INTERRUPT_POLARITY](ne-wudfinterrupt-_wdf_interrupt_polarity.md) | The WDF_INTERRUPT_POLARITY enumeration type is used to specify an interrupt signal's polarity. |
| [_WDF_INTERRUPT_POLICY](ne-wudfinterrupt-_wdf_interrupt_policy.md) | The WDF_INTERRUPT_POLICY enumeration type identifies the affinity policies that the Plug and Play (PnP) manager can use when it assigns a device's interrupts to the processors of a multiprocessor system. |
| [_WDF_INTERRUPT_PRIORITY](ne-wudfinterrupt-_wdf_interrupt_priority.md) | The WDF_INTERRUPT_PRIORITY enumeration type identifies relative priorities for device interrupts. |