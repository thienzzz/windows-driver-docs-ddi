---
UID : NE:printerextension.tagPrintJobStatus
title : tagPrintJobStatus
author : windows-driver-content
description : This enumeration is a one-to-one mapping to the spooler flags suppled in the JOB_INFO_X structures.
old-location : print\printjobstatus.htm
old-project : print
ms.assetid : 856FDAE1-C1D9-458D-B386-0A2D8612EA33
ms.author : windowsdriverdev
ms.date : 1/8/2018
ms.keywords : tagPrintJobStatus, PrintJobStatus
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : printerextension.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 8.1
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PrintJobStatus
req.alt-loc : Printerextension.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= APC_LEVEL
req.typenames : PrintJobStatus
req.product : Windows 10 or later.
---

# tagPrintJobStatus Enumeration
This enumeration is a one-to-one mapping to the spooler flags suppled in the JOB_INFO_X structures.

For example, <a href="http://msdn.microsoft.com/en-us/library/windows/desktop/dd145019(v=vs.85).aspx">JOB_INFO_1</a> has the same set of status flags as shown in the following list.

## Syntax
````
typedef enum _PrintJobStatus { 
  PrintJobStatus_Paused              = 0x1,
  PrintJobStatus_Error               = 0x2,
  PrintJobStatus_Deleting            = 0x4,
  PrintJobStatus_Spooling            = 0x8,
  PrintJobStatus_Printing            = 0x10,
  PrintJobStatus_Offline             = 0x20,
  PrintJobStatus_PaperOut            = 0x40,
  PrintJobStatus_Printed             = 0x80,
  PrintJobStatus_Deleted             = 0x100,
  PrintJobStatus_BlockedDeviceQueue  = 0x200,
  PrintJobStatus_UserIntervention    = 0x400,
  PrintJobStatus_Restarted           = 0x800,
  PrintJobStatus_Complete            = 0x1000,
  PrintJobStatus_Retained            = 0x2000
} PrintJobStatus;
````

## Constants

<table>

<tr>
<td>PrintJobStatus_BlockedDeviceQueue</td>
<td>The driver cannot print the job.</td>
</tr>

<tr>
<td>PrintJobStatus_Complete</td>
<td>The job data transfer to the printer is complete. Note that  the printing of the job may not yet be complete.</td>
</tr>

<tr>
<td>PrintJobStatus_Deleted</td>
<td>The job has been deleted.</td>
</tr>

<tr>
<td>PrintJobStatus_Deleting</td>
<td>The job is being deleted.</td>
</tr>

<tr>
<td>PrintJobStatus_Error</td>
<td>There is an error associated with the job.</td>
</tr>

<tr>
<td>PrintJobStatus_Offline</td>
<td>The printer is offline.</td>
</tr>

<tr>
<td>PrintJobStatus_PaperOut</td>
<td>The printer is out of paper.</td>
</tr>

<tr>
<td>PrintJobStatus_Paused</td>
<td>The job is paused.</td>
</tr>

<tr>
<td>PrintJobStatus_Printed</td>
<td>The job printing is completed.</td>
</tr>

<tr>
<td>PrintJobStatus_Printing</td>
<td>The job is printing.</td>
</tr>

<tr>
<td>PrintJobStatus_Restarted</td>
<td>The job has been restarted.</td>
</tr>

<tr>
<td>PrintJobStatus_Retained</td>
<td>The job has been retained in the print queue and cannot be deleted.</td>
</tr>

<tr>
<td>PrintJobStatus_Spooling</td>
<td>The job is spooling.</td>
</tr>

<tr>
<td>PrintJobStatus_UserIntervention</td>
<td>The printer has an error that requires intervention from the user.</td>
</tr>
</table>

## Remarks

A <b>PrintJobStatus_Retained</b> flag can be raised for several reasons. For example, jobs could be kept in the queue if the administrator of the queue used the desktop print queue UI to set the “Keep Printed Jobs” feature to be on.

It is possible for a job to have multiple  flag values specified simultaneously.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | printerextension.h |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/3C806C3B-78A1-44B6-A9AC-E7258D216637">IPrintJob::Status</a>
</dt>
<dt><a href="http://msdn.microsoft.com/en-us/library/windows/desktop/dd145019(v=vs.85).aspx">JOB_INFO_1</a></dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20PrintJobStatus enumeration%20 RELEASE:%20(1/8/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>