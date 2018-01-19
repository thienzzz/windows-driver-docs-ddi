---
UID : NE:pepfx._GPIO_PIN_IORESTRICTION_TYPE
title : _GPIO_PIN_IORESTRICTION_TYPE
author : windows-driver-content
description : The GPIO_PIN_IORESTRICTION_TYPE enumeration describes the functions that a GPIO pin is limited to performing.
old-location : kernel\gpio_pin_iorestriction_type.htm
old-project : kernel
ms.assetid : 381A59EE-BA1C-4810-842B-1D3E4D964486
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _GPIO_PIN_IORESTRICTION_TYPE, GPIO_PIN_IORESTRICTION_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : pepfx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Supported starting with Windows 10.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : GPIO_PIN_IORESTRICTION_TYPE
req.alt-loc : pepfx.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : See Remarks.
req.typenames : GPIO_PIN_IORESTRICTION_TYPE
---

# _GPIO_PIN_IORESTRICTION_TYPE Enumeration
The <b>GPIO_PIN_IORESTRICTION_TYPE</b> enumeration describes the functions that a GPIO pin is limited to performing.

## Syntax
````
typedef enum _GPIO_PIN_IORESTRICTION_TYPE { 
  IoRestrictionNone,
  IoRestrictionInputOnly,
  IoRestrictionOutputOnly,
  IoRestrictionNoneAndPreserve
} GPIO_PIN_IORESTRICTION_TYPE;
````

## Constants

<table>

<tr>
<td>IoRestrictionInputOnly</td>
<td>Indicates that the GPIO pin is restricted to input.</td>
</tr>

<tr>
<td>IoRestrictionNone</td>
<td>Indicates that the GPIO pin is not restricted to either input or output. When no IO restriction is described, it is assumed to be <b>IoRestrictionNone</b>.</td>
</tr>

<tr>
<td>IoRestrictionNoneAndPreserve</td>
<td>Indicates that the GPIO pin is not restricted to either input or output and that the mode should be preserved when the driver is unloaded.</td>
</tr>

<tr>
<td>IoRestrictionOutputOnly</td>
<td>Indicates that the GPIO pin is restricted to output.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | pepfx.h |