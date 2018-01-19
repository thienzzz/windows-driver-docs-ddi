---
UID : NF:wdm.IoWMIOpenBlock
title : IoWMIOpenBlock function
author : windows-driver-content
description : The IoWMIOpenBlock routine opens the WMI data block object for the specified WMI class.
old-location : kernel\iowmiopenblock.htm
old-project : kernel
ms.assetid : c23d1861-59df-4bd4-a005-173ccac53049
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : IoWMIOpenBlock
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Ntddk.h, Ntifs.h. The WMIGUID_XXX values are declared in Wmistr.h. To use them, include Wmistr.h.
req.target-type : Universal
req.target-min-winverclnt : Available in Windows XP and later versions of the Windows operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoWMIOpenBlock
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
req.irql : <= APC_LEVEL
req.typenames : WORK_QUEUE_TYPE
req.product : Windows 10 or later.
---


# IoWMIOpenBlock function
The <b>IoWMIOpenBlock</b> routine opens the WMI data block object for the specified WMI class.

## Syntax

````
NTSTATUS IoWMIOpenBlock(
  _In_  GUID  *DataBlockGuid,
  _In_  ULONG DesiredAccess,
  _Out_ PVOID *DataBlockObject
);
````

## Parameters

`Guid`



`DesiredAccess`

Specifies the desired access rights to the data block object. The caller must have particular access rights to perform certain operations. 

The following is a description of each access right bit and the operations it allows:

`DataBlockObject`

Pointer to a memory location where the routine returns a pointer to the data block object.


## Return Value

Returns STATUS_SUCCESS on success, or the appropriate NTSTATUS error code on failure.

## Remarks

The caller uses <b>IoWMIOpenBlock</b> to create a data block object for the specified WMI class GUID. Subsequently, the caller can use the data block object to read or write WMI class properties, run WMI class methods, and register callbacks for WMI events.

Use the <b>IoWMIQuery<i>Xxx</i></b> and <b>IoWMISet<i>Xxx</i></b> routines to read and write WMI class properties. Use <a href="..\wdm\nf-wdm-iowmiexecutemethod.md">IoWMIExecuteMethod</a> to run WMI class methods, and use <a href="..\wdm\nf-wdm-iowmisetnotificationcallback.md">IoWMISetNotificationCallback</a> to register a WMI event notification callback.

Use <a href="..\wdm\nf-wdm-obdereferenceobject.md">ObDereferenceObject</a> to close the data block object once it is no longer needed.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Ntddk.h, Ntifs.h. The WMIGUID_XXX values are declared in Wmistr.h. To use them, include Wmistr.h.) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-iowmiexecutemethod.md">IoWMIExecuteMethod</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmiqueryalldata.md">IoWMIQueryAllData</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmiqueryalldatamultiple.md">IoWMIQueryAllDataMultiple</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmiquerysingleinstance.md">IoWMIQuerySingleInstance</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmiquerysingleinstancemultiple.md">IoWMIQuerySingleInstanceMultiple</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmisetnotificationcallback.md">IoWMISetNotificationCallback</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmisetsingleinstance.md">IoWMISetSingleInstance</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmisetsingleitem.md">IoWMISetSingleItem</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwclose.md">ZwClose</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IoWMIOpenBlock routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>