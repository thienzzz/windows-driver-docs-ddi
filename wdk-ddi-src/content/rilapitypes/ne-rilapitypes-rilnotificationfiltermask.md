---
UID : NE:rilapitypes.RILNOTIFICATIONFILTERMASK
title : RILNOTIFICATIONFILTERMASK
author : windows-driver-content
description : This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location : netvista\rilnotificationfiltermask_2.htm
old-project : netvista
ms.assetid : 00d083af-f2c1-4ad5-803a-5981ed70035f
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILNOTIFICATIONFILTERMASK, RILNOTIFICATIONFILTERMASK
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : rilapitypes.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILNOTIFICATIONFILTERMASK
req.alt-loc : rilapitypes.h
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
req.typenames : RILNOTIFICATIONFILTERMASK
req.product : Windows 10 or later.
---

# RILNOTIFICATIONFILTERMASK Enumeration
This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## Syntax
````
typedef enum _RILNOTIFICATIONFILTERMASK { 
  RIL_NFS_SIGNALQUALITY,
  RIL_NFS_REGSTATUS_RATKIND,
  RIL_NFS_LOCATIONUPDATE,
  RIL_NFS_ALL
} RILNOTIFICATIONFILTERMASK;
````

## Constants

<table>

<tr>
<td>RIL_NFS_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_NFS_LOCATIONUPDATE</td>
<td></td>
</tr>

<tr>
<td>RIL_NFS_REGSTATUS_RATKIND</td>
<td></td>
</tr>

<tr>
<td>RIL_NFS_SIGNALQUALITY</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapitypes.h |