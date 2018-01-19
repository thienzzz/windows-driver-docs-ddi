---
UID : NS:wpprecorder._RECORDER_CONFIGURE_PARAMS
title : _RECORDER_CONFIGURE_PARAMS
author : windows-driver-content
description : The RECORDER_CONFIGURE_PARAMS structure is an input parameter to the WppRecorderConfigure method to enable or disable the default log to which WPP prints.
old-location : devtest\recorder_configure_params.htm
old-project : devtest
ms.assetid : 9D2AB7D0-CD75-4539-9CB8-8CBA33EFE299
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _RECORDER_CONFIGURE_PARAMS, RECORDER_CONFIGURE_PARAMS, *PRECORDER_CONFIGURE_PARAMS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : wpprecorder.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RECORDER_CONFIGURE_PARAMS
req.alt-loc : Wpprecorder.h
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
req.typenames : RECORDER_CONFIGURE_PARAMS, *PRECORDER_CONFIGURE_PARAMS
req.product : Windows 10 or later.
---

# _RECORDER_CONFIGURE_PARAMS structure
The <b>RECORDER_CONFIGURE_PARAMS</b> structure is an input parameter to the <a href="..\wpprecorder\nf-wpprecorder-wpprecorderconfigure.md">WppRecorderConfigure</a> method to enable or disable the default log to which WPP prints.

## Syntax
````
typedef struct _RECORDER_CONFIGURE_PARAMS {
  ULONG   Size;
  BOOLEAN CreateDefaultLog;
} RECORDER_CONFIGURE_PARAMS, *PRECORDER_CONFIGURE_PARAMS;
````

## Members

        
            `CreateDefaultLog`

            Indicates whether WPP should use the default log for trace messages. TRUE (default), use the default log; FALSE disable the default log.
        
            `Size`

            Size of this structure.

    ## Remarks
        To initialize this structure, the caller must call <a href="..\wpprecorder\nf-wpprecorder-recorder_configure_params_init.md">RECORDER_CONFIGURE_PARAMS_INIT</a>.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wpprecorder.h |