---
UID : NF:wdm.IoWMIQuerySingleInstanceMultiple
title : IoWMIQuerySingleInstanceMultiple function
author : windows-driver-content
description : The IoWMIQuerySingleInstanceMultiple routine returns all WMI data block instances that implement the specified WMI classes with the specified instance names.
old-location : kernel\iowmiquerysingleinstancemultiple.htm
old-project : kernel
ms.assetid : c0e011b5-804c-4f0d-a125-a083a0f83d50
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : IoWMIQuerySingleInstanceMultiple
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : wdm.h
req.include-header : Wdm.h, Ntddk.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available in Windows XP and later versions of the Windows operating system.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IoWMIQuerySingleInstanceMultiple
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


# IoWMIQuerySingleInstanceMultiple function
The <b>IoWMIQuerySingleInstanceMultiple</b> routine returns all WMI data block instances that implement the specified WMI classes with the specified instance names.

## Syntax

````
NTSTATUS IoWMIQuerySingleInstanceMultiple(
  _In_      PVOID           *DataBlockObjectList,
  _In_      PUNICODE_STRING InstanceNames,
  _In_      ULONG           ObjectCount,
  _Inout_   ULONG           *InOutBufferSize,
  _Out_opt_ PVOID           OutBuffer
);
````

## Parameters

`DataBlockObjectList`

Pointer to an array of pointers of WMI data block objects. The caller opens a data block object for each WMI class with the <a href="..\wdm\nf-wdm-iowmiopenblock.md">IoWMIOpenBlock</a> routine. Each object must be opened with the WMIGUID_QUERY access right.

`InstanceNames`

Pointer to an array of <a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structures containing instance names. The <i>n</i>th instance name in the array corresponds to the value of the <b>InstanceName</b> property for the <i>n</i>th WMI class specified in the array pointed to by the <i>DataBlockObjectList</i> parameter.

`ObjectCount`

Specifies the number of entries in the arrays passed in the <i>DataBlockObjectList</i> and <i>InstanceNames</i> parameters.

`InOutBufferSize`

Pointer to a memory location that specifies the size of the buffer passed in the <i>OutBuffer</i> parameter. If the routine succeeds, it updates the memory location to specify the number of bytes actually stored in <i>OutBuffer</i>. If the routine fails with STATUS_BUFFER_TOO_SMALL, it returns the number of bytes required to return the data.

`OutBuffer`

Pointer to the buffer where the routine returns the WMI data. The routine returns a sequence of variable-sized <a href="..\wmistr\ns-wmistr-tagwnode_single_instance.md">WNODE_SINGLE_INSTANCE</a> structures, one for each data block instance. The <b>WnodeHeader.Linkage</b> member of each <b>WNODE_SINGLE_INSTANCE</b> structure contains the offset from the beginning of the current <b>WNODE_SINGLE_INSTANCE</b> to the beginning of the next <b>WNODE_SINGLE_INSTANCE</b>. The final block in the chain has <b>WnodeHeader.Linkage</b> set to zero. Each distinct data block instance corresponds to a single matching WMI class and instance name. <i>OutBuffer</i> must point to a buffer allocated from nonpaged pool.


## Return Value

The routine returns an NTSTATUS code. Possible return values include:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The operation succeeded. The routine returns the WMI data in the buffer pointed to by the <i>OutBuffer</i> parameter. The routine also returns the size, in bytes, of the returned data in the memory location pointed to by the <i>InOutBufferSize</i> parameter.
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>The buffer passed by the caller in the <i>OutBuffer</i> parameter is too small. The routine returns the required buffer size in the memory location pointed to by the <i>InOutBufferSize</i> parameter.

## Remarks

<b>IoWMIQuerySingleInstanceMultiple</b> determines which drivers might support the specified WMI classes and instance names, and issues an <a href="https://msdn.microsoft.com/library/windows/hardware/ff551718">IRP_MN_QUERY_SINGLE_INSTANCE</a> request to each such driver. Each driver that exports the data block instance with matching <b>InstanceName</b> property returns the appropriate data.

If no drivers implement any of the specified WMI classes and instance names, the routine returns STATUS_SUCCESS. It also returns a value of zero in the memory location pointed to by the <i>InOutBufferSize</i> parameter.

To query for a single WMI class and instance name, use the <a href="..\wdm\nf-wdm-iowmiquerysingleinstance.md">IoWMIQuerySingleInstance</a> routine. Drivers can use the <a href="..\wdm\nf-wdm-iowmisetsingleinstance.md">IoWMISetSingleInstance</a> routine to update a class instance.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h, Ntddk.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wdm\nf-wdm-iowmiopenblock.md">IoWMIOpenBlock</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmiquerysingleinstance.md">IoWMIQuerySingleInstance</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-iowmisetsingleinstance.md">IoWMISetSingleInstance</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551718">IRP_MN_QUERY_SINGLE_INSTANCE</a>
</dt>
<dt>
<a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IoWMIQuerySingleInstanceMultiple routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>