---
UID : NS:61883._CIP_FRAME
title : _CIP_FRAME
author : windows-driver-content
description : The CIP_FRAME structure describes a frame to be attached to an input or output plug.
old-location : ieee\cip_frame.htm
old-project : IEEE
ms.assetid : ac9efa58-fd38-43f2-85e6-577d58735847
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _CIP_FRAME, *PCIP_FRAME, CIP_FRAME
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : 61883.h
req.include-header : 61883.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : CIP_FRAME
req.alt-loc : 61883.h
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
req.typenames : "*PCIP_FRAME, CIP_FRAME"
---

# _CIP_FRAME structure
The CIP_FRAME structure describes a frame to be attached to an input or output plug.

## Syntax
````
typedef struct _CIP_FRAME {
  union {
    PVOID Reserved;
    PVOID pNext;
  };
  ULONG                 Flags;
  PCIP_VALIDATE_ROUTINE pfnValidate;
  PVOID                 ValidateContext;
  PCIP_NOTIFY_ROUTINE   pfnNotify;
  PVOID                 NotifyContext;
  CYCLE_TIME            Timestamp;
  ULONG                 Status;
  PUCHAR                Packet;
  ULONG                 CompletedBytes;
} CIP_FRAME, *PCIP_FRAME;
````

## Members

        
            `CompletedBytes`

            
        
            `Flags`

            Specifies options associated with this frame. 

For packets to be received, <b>Flags</b> can be one of the following:
        
            `NotifyContext`

            Points to an optional caller-defined context for the caller-supplied function at <b>pfnNotify</b>. If the function does not require a context, <b>NotifyContext</b> can be <b>NULL</b>.
        
            `Packet`

            Points to the beginning of a caller-allocated data buffer to be transmitted or received with this frame. The frame length specified in the associated <a href="https://msdn.microsoft.com/library/windows/hardware/ff536950">Av61883_AttachFrame</a> request indicates the size of the buffer.
        
            `pfnNotify`

            Points to a caller-supplied function to be called by the protocol driver when the requested frame is completed. The protocol driver calls this function at IRQL = DISPATCH_LEVEL.

This function uses the following prototype:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>ULONG 
  (*PCIP_NOTIFY_ROUTINE) ( 
     IN PCIP_NOTIFY_INFO NotifyInfo 
 );</pre>
</td>
</tr>
</table></span></div>
        
            `pfnValidate`

            Points to a caller-supplied function to validate a source packet. This function uses the following prototype: The parameter <b>ValidateInfo</b> must point to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff537048">CIP_VALIDATE_INFO</a> structure that contains information about the frame. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>ULONG 
  (*PCIP_VALIDATE_ROUTINE) ( 
    IN PCIP_VALIDATE_INFO ValidateInfo
   );</pre>
</td>
</tr>
</table></span></div>
        
            `Status`

            The status of the frame. Can be one of the following:

CIP_STATUS_SUCCESS

CIP_STATUS_CORRUPT_FRAME

CIP_STATUS_FIRST_FRAME
        
            `Timestamp`

            The time associated with completion of the frame. 

For packets to be received, the protocol driver sets this member to the time when transmission of the frame was completed, unless CIP_USE_SOURCE_HEADER_TIMESTAMP is set in <b>Flags</b>. 

For packets to be transmitted, CIP-DV_STYLE_SYT or CIP_AUDIO_STYLE_SYT in <b>Flags</b> indicates the format of the timestamp.
        
            `ValidateContext`

            Points to an optional caller-defined context for the function at <b>pfnValidate</b>. If the function does not require a context, <b>ValidateContext</b> can be <b>NULL</b>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | 61883.h (include 61883.h) |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536950">Av61883_AttachFrame</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536956">Av61883_CancelFrame</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [IEEE\buses]:%20CIP_FRAME structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>