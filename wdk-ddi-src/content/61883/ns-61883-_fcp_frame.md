---
UID : NS:61883._FCP_FRAME
title : _FCP_FRAME
author : windows-driver-content
description : The FCP_FRAME structure describes a function control protocol (FCP) request.
old-location : ieee\fcp_frame.htm
old-project : IEEE
ms.assetid : 56a0e888-8048-4774-a46f-8a0beebfb9f2
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _FCP_FRAME, FCP_FRAME, *PFCP_FRAME
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
req.alt-api : FCP_FRAME
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
req.typenames : FCP_FRAME, *PFCP_FRAME
---

# _FCP_FRAME structure
The FCP_FRAME structure describes a function control protocol (FCP) request.

## Syntax
````
typedef struct _FCP_FRAME {
  UCHAR ctype  :4;
  UCHAR cts  :4;
  UCHAR payload[511];
} FCP_FRAME, *PFCP_FRAME;
````

## Members

        
            `cts`

            The CTS used for this FCP request. The CTS specifies the command set, the structure of the command/response field, and the rules of transactions used for sending FCP commands and responses.
        
            `ctype`

            The command or response type as defined by the Command/Transaction Set (CTS) used for this request.
        
            `payload`

            The FCP request for this frame.


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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536974">Av61883_GetFcpRequest</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536977">Av61883_GetFcpResponse</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536989">Av61883_SendFcpRequest</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536992">Av61883_SendFcpResponse</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [IEEE\buses]:%20FCP_FRAME structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>