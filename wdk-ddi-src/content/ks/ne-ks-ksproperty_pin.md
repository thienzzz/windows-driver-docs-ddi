---
UID : NE:ks.KSPROPERTY_PIN
title : KSPROPERTY_PIN
author : windows-driver-content
description : .
old-location : stream\ksproperty_pin.htm
old-project : stream
ms.assetid : C73B306C-A6DA-469A-984C-3FC605CC5E19
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : KSPROPERTY_PIN, KSPROPERTY_PIN
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ks.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KSPROPERTY_PIN
req.alt-loc : Ks.h
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
req.typenames : KSPROPERTY_PIN
---

# KSPROPERTY_PIN Enumeration


## Syntax
````
typedef enum  { 
  KSPROPERTY_PIN_CINSTANCES,
  KSPROPERTY_PIN_CTYPES,
  KSPROPERTY_PIN_DATAFLOW,
  KSPROPERTY_PIN_DATARANGES,
  KSPROPERTY_PIN_DATAINTERSECTION,
  KSPROPERTY_PIN_INTERFACES,
  KSPROPERTY_PIN_MEDIUMS,
  KSPROPERTY_PIN_COMMUNICATION,
  KSPROPERTY_PIN_GLOBALCINSTANCES,
  KSPROPERTY_PIN_NECESSARYINSTANCES,
  KSPROPERTY_PIN_PHYSICALCONNECTION,
  KSPROPERTY_PIN_CATEGORY,
  KSPROPERTY_PIN_NAME,
  KSPROPERTY_PIN_CONSTRAINEDDATARANGES,
  KSPROPERTY_PIN_PROPOSEDATAFORMAT,
  KSPROPERTY_PIN_PROPOSEDATAFORMAT2
} KSPROPERTY_PIN;
````

## Constants

<table>

<tr>
<td>KSPROPERTY_PIN_CATEGORY</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_CINSTANCES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_COMMUNICATION</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_CONSTRAINEDDATARANGES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_CTYPES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_DATAFLOW</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_DATAINTERSECTION</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_DATARANGES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_GLOBALCINSTANCES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_INTERFACES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_MEDIUMS</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_NAME</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_NECESSARYINSTANCES</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_PHYSICALCONNECTION</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_PROPOSEDATAFORMAT</td>
<td></td>
</tr>

<tr>
<td>KSPROPERTY_PIN_PROPOSEDATAFORMAT2</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ks.h |