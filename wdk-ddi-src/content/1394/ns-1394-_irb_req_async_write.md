---
UID : NS:1394._IRB_REQ_ASYNC_WRITE
title : _IRB_REQ_ASYNC_WRITE
author : windows-driver-content
description : This structure contains the fields necessary for the 1394 stack to carry out an asynchronous write request.
old-location : ieee\irb_req_async_write.htm
old-project : IEEE
ms.assetid : 007E0DDE-0BD1-499D-A6C6-446644BBCE00
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _IRB_REQ_ASYNC_WRITE, IRB_REQ_ASYNC_WRITE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : 1394.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IRB_REQ_ASYNC_WRITE
req.alt-loc : 1394.h
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
req.typenames : IRB_REQ_ASYNC_WRITE
---

# _IRB_REQ_ASYNC_WRITE structure
This structure contains the fields necessary for the 1394 stack to carry out an asynchronous write request.

## Syntax
````
typedef struct _IRB_REQ_ASYNC_WRITE {
  IO_ADDRESS DestinationAddress;
  ULONG      nNumberOfBytesToWrite;
  ULONG      nBlockSize;
  ULONG      fulFlags;
  PMDL       Mdl;
  ULONG      ulGeneration;
  UCHAR      chPriority;
  UCHAR      nSpeed;
  UCHAR      tCode;
  UCHAR      Reserved;
  ULONG      ElapsedTime;
} IRB_REQ_ASYNC_WRITE;
````

## Members

        
            `chPriority`

            Reserved.
        
            `DestinationAddress`

            Specifies the 1394 64-bit destination address for this write operation. The driver only must fill in the <b>IA_Destination_Offset</b> member of <b>u.AsyncWrite.DestinationAddress</b>; the bus driver fills in the <b>IA_Destination_ID</b> member. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff537346">IO_ADDRESS</a> for the structure description.
        
            `ElapsedTime`

            Elapsed time in nanoseconds. Only valid for flag <b>ASYNC_FLAGS_PING</b>.
        
            `fulFlags`

            Specifies any nondefault settings for this operation. The following flags are provided.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>
 ASYNC_FLAGS_NONINCREMENTING

</td>
<td>
Do not increment 1394 address during asynchronous operation. This flag is set only in large asynchronous requests (that is, those greater than asynchronous packet size).

</td>
</tr>
<tr>
<td>
ASYNC_FLAGS_NO_STATUS

</td>
<td>
Always return success from the write operation, whether the write succeeds or fails.

</td>
</tr>
<tr>
<td>
ASYNC_FLAGS_BROADCAST

</td>
<td>
Broadcast to all nodes on the bus.

</td>
</tr>
</table>
 

Use the bitwise operator OR to combine the settings.
        
            `Mdl`

            Points to an MDL that describes the device driver's buffer, which receives data from the 1394 node.
        
            `nBlockSize`

            Specifies the size of each individual block within the data stream that is written as a whole to the node. If this parameter is zero, then the maximum packet size for the speed selected is used in breaking up these write requests, unless raw-mode addressing is used.



If raw-mode addressing is used, the client driver should set the <b>nBlockSize</b> member to the maximum asynchronous payload size that is supported by the device at the connected speed. 

For more information on raw-mode addressing, see <a href="https://msdn.microsoft.com/93ad0cdf-5ac2-4916-b90e-1e64ca4494b6">Sending Asynchronous I/O Request Packets on the IEEE 1394 Bus.</a>


<div class="alert"><b>Note</b>  In Windows 7 and later versions of Windows, you can specify new values higher speed and  greater sized payloads. For more information, see <a href="buses.device_driver_interface__ddi__changes_in_windows_7#speed#speed">New Flags for Speed and Payload Size</a> and <a href="buses.device_driver_interface__ddi__changes_in_windows_7#ioctl#ioctl">IEEE 1394 IOCTL Changes</a> in Device Driver Interface (DDI) Changes in Windows 7.</div>
<div> </div>
        
            `nNumberOfBytesToWrite`

            Specifies the number of bytes to write to the 1394 node.
        
            `nSpeed`

            Reserved.
        
            `Reserved`

            Reserved.
        
            `tCode`

            Reserved.
        
            `ulGeneration`

            Specifies the bus reset generation as known by the device driver that submitted this asynchronous request. If the generation count specified does not match the actual generation of the bus, this request is returned with a status of STATUS_INVALID_GENERATION.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | 1394.h |