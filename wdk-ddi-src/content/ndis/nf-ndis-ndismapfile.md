---
UID : NF:ndis.NdisMapFile
title : NdisMapFile function
author : windows-driver-content
description : The NdisMapFile function maps an already open file into a caller-accessible buffer if the file is currently unmapped.
old-location : netvista\ndismapfile.htm
old-project : netvista
ms.assetid : 965bb4c7-826d-425b-b10d-2d5a29ca0f91
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : NdisMapFile
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ndis.h
req.include-header : Ndis.h
req.target-type : Universal
req.target-min-winverclnt : Supported for NDIS 6.0 and NDIS 5.1 drivers (see    NdisMapFile (NDIS 5.1)) in Windows   Vista. Supported for NDIS 5.1 drivers (see    NdisMapFile (NDIS 5.1)) in Windows   XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NdisMapFile
req.alt-loc : ndis.lib,ndis.dll
req.ddi-compliance : Irql_Miscellaneous_Function
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ndis.lib
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---


# NdisMapFile function
The 
  <b>NdisMapFile</b> function maps an already open file into a caller-accessible buffer if the file is
  currently unmapped.

## Syntax

````
VOID NdisMapFile(
  _Out_ PNDIS_STATUS Status,
  _Out_ PVOID *      MappedBuffer,
  _In_  NDIS_HANDLE  FileHandle
);
````

## Parameters

`Status`

A pointer to a caller-supplied variable in which this function returns the status of the mapping
     operation, which can be one of the following:

`MappedBuffer`

A pointer to a caller-supplied variable in which this function returns the base virtual address of
     the mapped file contents or <b>NULL</b>.

`FileHandle`

The handle that was returned by a preceding call to the 
     <a href="..\ndis\nf-ndis-ndisopenfile.md">NdisOpenFile</a> function.


## Return Value

None

## Remarks

<b>NdisMapFile</b> associates (maps) a virtual address range with an opened file so the driver can access
    the file contents. 
    <b>NdisMapFile</b> allows only one mapping of a particular file to be outstanding at any time.
    Consequently, a successful caller is given exclusive access to the file data until 
    <b>NdisUnmapFile</b> or the 
    <a href="..\ndis\nf-ndis-ndisclosefile.md">NdisCloseFile</a> function is called.

A miniport driver can map and unmap such an open file as necessary, using alternating calls to 
    <b>NdisMapFile</b> and 
    <a href="..\ndis\nf-ndis-ndisunmapfile.md">NdisUnmapFile</a>. A call to 
    <b>NdisCloseFile</b> releases the 
    <i>FileHandle</i> and deallocates the buffer containing the file contents.

A miniport driver can call 
    <b>NdisMapFile</b> only during initialization.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ndis.h (include Ndis.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** | Irql_Miscellaneous_Function |

## See Also

<dl>
<dt>
<a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisclosefile.md">NdisCloseFile</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisopenfile.md">NdisOpenFile</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisunmapfile.md">NdisUnmapFile</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NdisMapFile function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>