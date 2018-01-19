---
UID : NS:ksmedia.tagKS_MPEG1VIDEOINFO
title : tagKS_MPEG1VIDEOINFO
author : windows-driver-content
description : The KS_MPEG1VIDEOINFO structure describes an MPEG-1 video stream.
old-location : stream\ks_mpeg1videoinfo.htm
old-project : stream
ms.assetid : 301b954a-4e50-4a04-a575-17d7d54fa691
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : tagKS_MPEG1VIDEOINFO, KS_MPEG1VIDEOINFO, *PKS_MPEG1VIDEOINFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ksmedia.h
req.include-header : Ksmedia.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KS_MPEG1VIDEOINFO
req.alt-loc : ksmedia.h
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
req.typenames : KS_MPEG1VIDEOINFO, *PKS_MPEG1VIDEOINFO
---

# tagKS_MPEG1VIDEOINFO structure
The KS_MPEG1VIDEOINFO structure describes an MPEG-1 video stream.

## Syntax
````
typedef struct tagKS_MPEG1VIDEOINFO {
  KS_VIDEOINFOHEADER hdr;
  DWORD              dwStartTimeCode;
  DWORD              cbSequenceHeader;
  BYTE               bSequenceHeader[1];
} KS_MPEG1VIDEOINFO, *PKS_MPEG1VIDEOINFO;
````

## Members

        
            `bSequenceHeader`

            The length of the <b>bSequenceHeader</b> member, in bytes.
        
            `cbSequenceHeader`

            The length of the <b>bSequenceHeader</b> member, in bytes.
        
            `dwStartTimeCode`

            A 25-bit "group-of-pictures" time code at the start of data.
        
            `hdr`

            Specifies a <a href="..\ksmedia\ns-ksmedia-tagks_videoinfoheader.md">KS_VIDEOINFOHEADER</a> structure that describes the details of the video stream.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ksmedia.h (include Ksmedia.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ksmedia\ns-ksmedia-tagks_videoinfoheader.md">KS_VIDEOINFOHEADER</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KS_MPEG1VIDEOINFO structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>