---
UID : NE:fwpsk.FWPS_FIELDS_STREAM_V4_
title : FWPS_FIELDS_STREAM_V4_
author : windows-driver-content
description : The FWPS_FIELDS_STREAM_V4 enumeration type specifies the data field identifiers for the FWPS_LAYER_STREAM_V4 and FWPS_LAYER_STREAM_V4_DISCARD run-time filtering layers.
old-location : netvista\fwps_fields_stream_v4.htm
old-project : netvista
ms.assetid : 1225f28d-3b89-4b14-82c3-5162de9fe8fd
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FWPS_FIELDS_STREAM_V4_, FWPS_FIELDS_STREAM_V4
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Unless otherwise noted, supported starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FWPS_FIELDS_STREAM_V4
req.alt-loc : fwpsk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : FWPS_FIELDS_STREAM_V4
---

# FWPS_FIELDS_STREAM_V4_ Enumeration
The FWPS_FIELDS_STREAM_V4 enumeration type specifies the data field identifiers for the
  FWPS_LAYER_STREAM_V4 and FWPS_LAYER_STREAM_V4_DISCARD 
  <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa366492">run-time filtering layers</a>.

## Syntax
````
typedef enum FWPS_FIELDS_STREAM_V4_ { 
  FWPS_FIELD_STREAM_V4_IP_LOCAL_ADDRESS,
  FWPS_FIELD_STREAM_V4_IP_LOCAL_ADDRESS_TYPE,
  FWPS_FIELD_STREAM_V4_IP_REMOTE_ADDRESS,
  FWPS_FIELD_STREAM_V4_IP_LOCAL_PORT,
  FWPS_FIELD_STREAM_V4_IP_REMOTE_PORT,
  FWPS_FIELD_STREAM_V4_DIRECTION,
#if (NTDDI_VERSION >= NTDDI_WIN6SP1
  FWPS_FIELD_STREAM_V4_FLAGS,
#endif 
  FWPS_FIELD_STREAM_V4_MAX
} FWPS_FIELDS_STREAM_V4;
````

## Constants

<table>

<tr>
<td>FWPS_FIELD_STREAM_V4_DIRECTION</td>
<td></td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_FLAGS</td>
<td>A bitwise OR of a combination of filtering condition flags. For information about the possible
     flags, see 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff549942">Filtering Condition Flags</a>.
     

<div class="alert"><b>Note</b>  Supported in Windows Server 2008, Windows Vista SP1, and later versions of
     Windows.</div>
<div> </div></td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_IP_LOCAL_ADDRESS</td>
<td>The local IP address.</td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_IP_LOCAL_ADDRESS_TYPE</td>
<td>The local IP address type. The possible values are defined by the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a> enumeration.</td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_IP_LOCAL_PORT</td>
<td>The local transport protocol port number.</td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_IP_REMOTE_ADDRESS</td>
<td>The remote IP address.</td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_IP_REMOTE_PORT</td>
<td>The remote transport protocol port number.</td>
</tr>

<tr>
<td>FWPS_FIELD_STREAM_V4_MAX</td>
<td>The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.</td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff568757">NL_ADDRESS_TYPE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_FIELDS_STREAM_V4 enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>