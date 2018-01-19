---
UID : NE:urstypes._URS_ROLE
title : _URS_ROLE
author : windows-driver-content
description : Defines values for roles supported by a USB dual-role controller.
old-location : buses\urs_role.htm
old-project : usbref
ms.assetid : A1ED9DBD-67FF-4AE7-8E5E-016C2C89A79E
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _URS_ROLE, *PURS_ROLE, URS_ROLE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : urstypes.h
req.include-header : Urstypes.h
req.target-type : Windows
req.target-min-winverclnt : Windows 10
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 1.15
req.umdf-ver : 
req.alt-api : URS_ROLE, *PURS_ROLE
req.alt-loc : Urstypes.h
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
req.typenames : "*PURS_ROLE, URS_ROLE"
req.product : Windows 10 or later.
---

# _URS_ROLE Enumeration
Defines values for roles supported by a USB dual-role controller.

## Syntax
````
typedef enum _URS_ROLE { 
  UrsRoleNone      = 0,
  UrsRoleHost,
  UrsRoleFunction
} URS_ROLE, *PURS_ROLE;
````

## Constants

<table>

<tr>
<td>UrsRoleFunction</td>
<td>Indicates the function role of the controller.</td>
</tr>

<tr>
<td>UrsRoleHost</td>
<td>Indicates the host role of the controller.</td>
</tr>

<tr>
<td>UrsRoleNone</td>
<td>Internal use only. Must be 0.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** | 1.15 |
| **Minimum UMDF version** |  |
| **Header** | urstypes.h (include Urstypes.h) |