---
UID : NF:scsiwmi.ScsiPortWmiSetData
title : ScsiPortWmiSetData function
author : windows-driver-content
description : The ScsiPortWmiSetData routine updates the WNODE_ALL_DATA structure within the request context to specify the position and length of the data for an instance.
old-location : storage\scsiportwmisetdata.htm
old-project : storage
ms.assetid : eb4578c9-48e5-4113-ba58-a3d71052f782
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : ScsiPortWmiSetData
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : scsiwmi.h
req.include-header : Miniport.h, Scsi.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : ScsiPortWmiSetData
req.alt-loc : Scsiwmi.h
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
req.typenames : SCSIWMI_ENABLE_DISABLE_CONTROL
req.product : Windows 10 or later.
---


# ScsiPortWmiSetData function
The <b>ScsiPortWmiSetData</b> routine updates the <a href="..\wmistr\ns-wmistr-tagwnode_all_data.md">WNODE_ALL_DATA</a> structure within the request context to specify the position and length of the data for an instance.

## Syntax

````
PVOID ScsiPortWmiSetData(
  _In_    PSCSIWMI_REQUEST_CONTEXT RequestContext,
  _In_    ULONG                    InstanceIndex,
  _In_    ULONG                    DataLength,
  _Out_   PULONG                   BufferAvail,
  _Inout_ PULONG                   SizeNeeded
);
````

## Parameters

`RequestContext`

Pointer to a structure of type <a href="..\scsiwmi\ns-scsiwmi-scsiwmi_request_context.md">SCSIWMI_REQUEST_CONTEXT</a> that contains the request context for a WMI SRB.

`InstanceIndex`

Contains an index that indicates the instance for which the position and length of the instance data are to be specified.

`DataLength`

Specifies the number of bytes  of data required to describe the instance.

`BufferAvail`

Must contain, on input, the number of bytes of buffer space in the <a href="..\wmistr\ns-wmistr-tagwnode_all_data.md">WNODE_ALL_DATA</a> structure that can be used for describing instance names and data. On return, this member contains the number of bytes of buffer space that remain. 

There are three SCSI Port WMI routines that return a value for the available buffer size in their <i>BufferAvail </i>parameter:


<a href="..\scsiwmi\nf-scsiwmi-scsiportwmisetinstancecount.md">ScsiPortWmiSetInstanceCount</a>


<b>ScsiPortWmiSetData</b>


<a href="..\scsiwmi\nf-scsiwmi-scsiportwmisetinstancename.md">ScsiPortWmiSetInstanceName</a>


The miniport driver must call <b>ScsiPortWmiSetInstanceCount</b> first, but after <b>ScsiPortWmiSetInstanceCount</b> has been called, it does not matter in what order the minidriver calls <b>ScsiPortWmiSetData</b> and <b>ScsiPortWmiSetInstanceName</b>. When calling either <b>ScsiPortWmiSetData</b> or <b>ScsiPortWmiSetInstanceName</b>, the value passed to the routine in its <i>BufferAvail </i>parameter must be the same as the value returned in the <i>BufferAvail </i>parameter by the most recently called SCSI Port WMI routine. For instance, suppose the minidriver calls <b>ScsiPortWmiSetInstanceCount</b> first, and this routine returns a value of 1,000 in its <i>BufferAvail </i>parameter. Next, the minidriver calls <b>ScsiPortWmiSetData</b> which returns a value of 500 in its <i>BufferAvail </i>parameter. Finally, the minidriver calls <b>ScsiPortWmiSetInstanceName</b> which returns a value of 200 in its <i>BufferAvail </i>parameter. The initial value of 1,000 must be passed to <b>ScsiPortWmiSetData</b> in <i>BufferAvail</i>, and the value of 500 must be passed to <b>ScsiPortWmiSetInstanceName</b>. 

If there is not enough memory available to add new instance data of size <i>DataLength</i> bytes<i>, </i>a zero will be returned in the <i>BufferAvail</i> member.

`SizeNeeded`

Indicates, on input,  the number of bytes needed to describe the entire WNODE <i>before </i>adding the descriptive data for the instance specified by <i>InstanceIndex</i>. On return, this member will contain the size of the WNODE, including the data for the new instance.


## Return Value

The <b>ScsiPortWmiSetData</b> routine returns a pointer to the buffer where the caller can store descriptive information about the instance identified by <i>InstanceIndex</i>. If <b>ScsiPortWmiSetData</b> cannot allocate enough memory for the instance data, or if the WNODE contained within the request context is not of type <a href="..\wmistr\ns-wmistr-tagwnode_all_data.md">WNODE_ALL_DATA</a>, <b>ScsiPortWmiSetData</b> returns <b>NULL</b>.

## Remarks

The minidriver must call <a href="..\scsiwmi\nf-scsiwmi-scsiportwmisetinstancecount.md">ScsiPortWmiSetInstanceCount</a> before calling <b>ScsiPortWmiSetData</b>.

The parameter <b>RequestContext</b> points to a request context structure, <a href="..\scsiwmi\ns-scsiwmi-scsiwmi_request_context.md">SCSIWMI_REQUEST_CONTEXT</a>, that contains information associated with a <a href="https://msdn.microsoft.com/5c2ed322-0fc9-4004-9a5f-f4d3c6a59fe9">Windows Management Instrumentation</a> (WMI) SCSI request block (SRB). The request context structure, in turn, contains one of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566371">WMI WNODE_XXX Structures</a> that is used by the WMI system to pass data between user-mode data consumers and kernel-mode data providers such as drivers. 

The <b>ScsiPortWmiSetData</b> routine requires the WNODE structure that is defined within the request context to be of type <a href="..\wmistr\ns-wmistr-tagwnode_all_data.md">WNODE_ALL_DATA</a>. This is because <b>ScsiPortWmiSetData</b> can specify the location and length of the data buffers for any of the instances associated with a WMI data block. Unlike the <a href="..\wmistr\ns-wmistr-tagwnode_single_instance.md">WNODE_SINGLE_INSTANCE</a> structure which contains information about a single instance, the WNODE_ALL_DATA structure contains an array of pointers to buffer areas for multiple instances, and <b>ScsiPortWmiSetData</b> uses the <i>InstanceIndex </i>parameter as an index into this array to initialize the appropriate array element for a particular instance. Each array element, once initialized, contains the size and location of a buffer area for an instance. 

The memory allocated for the request context must remain valid until after the miniport driver calls <b>ScsiPortWmiPostProcess</b>, and <b>ScsiPortWmiPostProcess</b> returns the final SRB status and buffer size. If the SRB can pend, the memory for the request context should be allocated from the SRB extension. If the SRB cannot pend, the memory can be allocated from a stack frame that does not go out of scope.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | scsiwmi.h (include Miniport.h, Scsi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\scsiwmi\ns-scsiwmi-scsiwmi_request_context.md">SCSIWMI_REQUEST_CONTEXT</a>
</dt>
<dt>
<a href="..\wmistr\ns-wmistr-tagwnode_single_instance.md">WNODE_SINGLE_INSTANCE</a>
</dt>
<dt>
<a href="..\wmistr\ns-wmistr-tagwnode_all_data.md">WNODE_ALL_DATA</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20ScsiPortWmiSetData routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>