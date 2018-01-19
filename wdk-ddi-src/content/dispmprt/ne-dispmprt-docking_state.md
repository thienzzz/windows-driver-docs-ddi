---
UID : NE:dispmprt.DOCKING_STATE
title : DOCKING_STATE
author : windows-driver-content
description : The DOCKING_STATE enumeration is used to describe the state of a portable computer that can be attached to a docking station.
old-location : display\docking_state.htm
old-project : display
ms.assetid : 4e051d49-57ae-43c8-a894-a6c2c277dce9
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : DOCKING_STATE, DOCKING_STATE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : dispmprt.h
req.include-header : Dispmprt.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DOCKING_STATE
req.alt-loc : dispmprt.h
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
req.typenames : DOCKING_STATE
---

# DOCKING_STATE Enumeration
The DOCKING_STATE enumeration is used to describe the state of a portable computer that can be attached to a docking station.

## Syntax
````
typedef enum  { 
  DockStateUnsupported  = 0,
  DockStateUnDocked     = 1,
  DockStateDocked       = 2,
  DockStateUnknown      = 3
} DOCKING_STATE;
````

## Constants

<table>

<tr>
<td>DockStateDocked</td>
<td>Indicates that the portable computer is docked.</td>
</tr>

<tr>
<td>DockStateUnDocked</td>
<td>Indicates that the portable computer is not docked.</td>
</tr>

<tr>
<td>DockStateUnknown</td>
<td>Indicates that the docking state of the portable computer is not known.</td>
</tr>

<tr>
<td>DockStateUnsupported</td>
<td>Indicates that the portable computer does not support docking.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dispmprt.h (include Dispmprt.h) |