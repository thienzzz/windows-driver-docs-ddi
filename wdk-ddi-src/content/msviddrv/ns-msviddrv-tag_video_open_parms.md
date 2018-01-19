---
UID : NS:msviddrv.tag_video_open_parms
title : tag_video_open_parms
author : windows-driver-content
description : .
old-location : stream\video_open_parms.htm
old-project : stream
ms.assetid : BD11B67F-9229-4584-A20D-7D7C70B42977
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : tag_video_open_parms, VIDEO_OPEN_PARMS, *LPVIDEO_OPEN_PARMS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : msviddrv.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : VIDEO_OPEN_PARMS
req.alt-loc : Msviddrv.h
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
req.typenames : VIDEO_OPEN_PARMS, *LPVIDEO_OPEN_PARMS
---

# tag_video_open_parms structure


## Syntax
````
typedef struct tag_video_open_parms {
  DWORD  dwSize;
  FOURCC fccType;
  FOURCC fccComp;
  DWORD  dwVersion;
  DWORD  dwFlags;
  DWORD  dwError;
  LPVOID pV1Reserved;
  LPVOID pV2Reserved;
  DWORD  dnDevNode;
} VIDEO_OPEN_PARMS, *LPVIDEO_OPEN_PARMS;
````

## Members

        
            `dnDevNode`

            Specifies the devnode for PnP devices.
        
            `dwError`

            If open fails, specifies why it failed.
        
            `dwFlags`

            Specifies the type of channel.
        
            `dwSize`

            Set to the size of the <b>VIDEO_OPEN_PARMS</b> structure.
        
            `dwVersion`

            Specifies the version of msvideo.
        
            `fccComp`

            This member is not used.
        
            `fccType`

            'vcap'
        
            `pV1Reserved`

            Reserved.
        
            `pV2Reserved`

            Reserved.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | msviddrv.h |