---
UID : NE:rilapitypes.RILUICCLOCKSTATEPARAMMASK
title : RILUICCLOCKSTATEPARAMMASK
author : windows-driver-content
description : This enumeration describes the RILUICCLOCKSTATEPARAMMASK.
old-location : netvista\riluicclockstateparammask.htm
old-project : netvista
ms.assetid : 19366fbe-8a04-4a9f-9acc-8de0211e6e0d
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : RILUICCLOCKSTATEPARAMMASK, RILUICCLOCKSTATEPARAMMASK
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : rilapitypes.h
req.include-header : Rilapitypes.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RILUICCLOCKSTATEPARAMMASK
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
req.typenames : RILUICCLOCKSTATEPARAMMASK
req.product : Windows 10 or later.
---

# RILUICCLOCKSTATEPARAMMASK Enumeration


## Syntax
````
enum RILUICCLOCKSTATEPARAMMASK {
  RIL_PARAM_UICCLOCKSTATE_UICCLOCK             = 0x00000001, 
  RIL_PARAM_UICCLOCKSTATE_LOCKSTATE            = 0x00000002, 
  RIL_PARAM_UICCLOCKSTATE_VERIFYATTEMPTSLEFT   = 0x00000004, 
  RIL_PARAM_UICCLOCKSTATE_UNBLOCKATTEMPTSLEFT  = 0x00000008, 
  RIL_PARAM_UICCLOCKSTATE_ALL                  = 0x0000000F 

};
````

## Constants

<table>

<tr>
<td>RIL_PARAM_UICCLOCKSTATE_ALL</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_UICCLOCKSTATE_LOCKSTATE</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_UICCLOCKSTATE_UICCLOCK</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_UICCLOCKSTATE_UNBLOCKATTEMPTSLEFT</td>
<td></td>
</tr>

<tr>
<td>RIL_PARAM_UICCLOCKSTATE_VERIFYATTEMPTSLEFT</td>
<td></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | rilapitypes.h (include Rilapitypes.h) |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn946509">Cellular COM enumerations</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20RILUICCLOCKSTATEPARAMMASK enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>