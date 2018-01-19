---
UID : NF:wdm.ExLocalTimeToSystemTime
title : ExLocalTimeToSystemTime function
author : windows-driver-content
description : The ExLocalTimeToSystemTime routine converts a system time value for the current time zone to an unbiased, GreenGMT value.
old-location : kernel\exlocaltimetosystemtime.htm
old-project : kernel
ms.assetid : ef4fcb57-2960-4cd3-9abc-f8c5bc46e1a3
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : ExLocalTimeToSystemTime
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available starting with Windows 2000.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ExLocalTimeToSystemTime
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : Any level
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# ExLocalTimeToSystemTime function
The <b>ExLocalTimeToSystemTime</b> routine converts a system time value for the current time zone to an unbiased, GreenGMT value.

## Syntax

````
VOID ExLocalTimeToSystemTime(
  _In_  PLARGE_INTEGER LocalTime,
  _Out_ PLARGE_INTEGER SystemTime
);
````

## Parameters

`LocalTime`

A pointer to a variable set to the locale-specific time.

`SystemTime`

A pointer to the returned value for GMT system time.


## Return Value

None

## Remarks

<b>ExLocalTimeToSystemTime</b> adds the time-zone bias at the current locale to compute the corresponding GMT system time value.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | Any level |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-exsystemtimetolocaltime.md">ExSystemTimeToLocalTime</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ExLocalTimeToSystemTime routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>