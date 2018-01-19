---
UID : NC:poclass.DEVICE_PASSIVE_COOLING
title : DEVICE_PASSIVE_COOLING
author : windows-driver-content
description : The PassiveCooling callback routine controls the degree to which the device must throttle its performance to meet cooling requirements.
old-location : kernel\passivecooling.htm
old-project : kernel
ms.assetid : 17ADC83B-53C8-43BD-9FFB-1197501FE275
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _PMI_THRESHOLD_CONFIGURATION, PMI_THRESHOLD_CONFIGURATION, *PPMI_THRESHOLD_CONFIGURATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : poclass.h
req.include-header : Poclass.h
req.target-type : Desktop
req.target-min-winverclnt : Supported starting with Windows 8.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PassiveCooling
req.alt-loc : Poclass.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : Called at PASSIVE_LEVEL.
req.typenames : PMI_THRESHOLD_CONFIGURATION, *PPMI_THRESHOLD_CONFIGURATION
---


# DEVICE_PASSIVE_COOLING function
The <i>PassiveCooling</i> callback routine controls the degree to which the device must throttle its performance to meet cooling requirements.

## Syntax

```
DEVICE_PASSIVE_COOLING DevicePassiveCooling;

void DevicePassiveCooling(
  PVOID Context,
  ULONG Percentage
)
{...}
```

## Parameters

`Context`

A pointer to interface-specific context information. The caller sets this parameter to the value of the <b>Context</b> member of the <a href="..\poclass\ns-poclass-_thermal_cooling_interface.md">THERMAL_COOLING_INTERFACE</a> structure that the driver previously supplied to the caller.

`Percentage`

The percentage of full performance at which the device is permitted to operate. A parameter value of 100 indicates that the device is under no cooling restrictions and can operate at full performance level. A parameter value of zero indicates that the device must operate at its lowest thermal level. A parameter value between 0 and 100 indicates the degree to which the device's performance must be throttled to reduce heat generation. This parameter value is a threshold that the device must not exceed.


## Return Value

None.

## Remarks

The driver for a device that has passive-cooling capabilities can implement this routine to enable the operating system to throttle the performance of the device, as necessary, to allow the device to cool.

For example, a device might be throttled by lowering the frequency of the clock that drives the device, by turning off one or more functional units in the device, or by lowering the voltage level on the power rail that supplies power to the device. Throttling a device to decrease the amount of heat that it generates tends to reduce the performance of the device.

The <i>Percentage</i> parameter is a value in the range 0 to 100 that indicates the degree to which the device is throttled. At <i>Percentage</i> = 0, the device is throttled so that it operates at its lowest performance level and generates the minimum amount of heat. At <i>Percentage</i> = 100, the device is not throttled at all; in this mode, the device operates at its full performance level and generates the maximum amount of heat.

A <i>Percentage</i> value between 0 and 100 indicates the percentage of full performance at which the device should operate. For example, a <i>Percentage</i> value of 50 indicates that the device should operate in a passive-power mode in which the heat generated by the device is roughly halfway between the heat generated at the <i>Percentage</i> = 0 and <i>Percentage</i> = 100 settings.

The device must operate at a level that does not exceed the <i>Percentage</i> value specified by the caller—unless the hardware cannot do so safely. For example, if a device can operate at only five different settings that correspond to <i>Percentage</i> values of 0, 25, 50, 75, and 100, and the caller specifies <i>Percentage</i> = 70, the driver must configure the device to operate at the setting that corresponds to <i>Percentage</i> = 50.

Initially, before the first call to the <i>PassiveCooling</i> routine, the device is configured to operate at its full performance level, with no throttling.

The driver for a device that does not have passive-cooling capabilities should set the <b>PassiveCooling</b> member of the <b>THERMAL_COOLING_INTERFACE</b> structure to <b>NULL</b>.

For more information about passive cooling, see <a href="https://msdn.microsoft.com/library/windows/hardware/hh698271">Passive and Active Cooling Modes</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | poclass.h (include Poclass.h) |
| **Library** |  |
| **IRQL** | Called at PASSIVE_LEVEL. |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\poclass\ns-poclass-_thermal_cooling_interface.md">THERMAL_COOLING_INTERFACE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20DEVICE_PASSIVE_COOLING routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>