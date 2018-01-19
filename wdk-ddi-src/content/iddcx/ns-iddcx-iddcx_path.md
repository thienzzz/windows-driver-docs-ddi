---
UID : NS:iddcx.IDDCX_PATH
title : IDDCX_PATH
author : windows-driver-content
description : Call IDDCX_PATH_INIT to initialize this structure.
old-location : display\iddcx_path.htm
old-project : display
ms.assetid : c0126718-6bb0-493c-9fdd-78ae372f8fd4
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : IDDCX_PATH,
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : iddcx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDDCX_PATH
req.alt-loc : iddcx.h
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
req.typenames : 
---

# IDDCX_PATH structure
Call <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt761937">IDDCX_PATH_INIT</a> to initialize this structure.

## Syntax
````
typedef struct IDDCX_PATH {
  UINT                            Size;
  IDDCX_MONITOR                   MonitorObject;
  IDDCX_PATH_FLAGS                Flags;
  DISPLAYCONFIG_VIDEO_SIGNAL_INFO TargetVideoSignalInfo;
} IDDCX_PATH, *IDDCX_PATH;
````

## Members

        
            `Flags`

            Contains flags for this path, like the path's active state and whether it changed.
        
            `MonitorObject`

            The handle the driver provides to identify the monitor this path is targeted at.
        
            `Size`

            Total size of the structure.
        
            `TargetVideoSignalInfo`

            The details of the target mode signal.

    ## Remarks
        The <a href="https://msdn.microsoft.com/library/windows/hardware/ff554007">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> value <b>vSyncFreq</b> is the Vsync rate between the Indirect Display device and the connected monitor.  <b>vSyncFreqDivider</b> is used to calculate the rate at which the OS will update the desktop image.

The desktop update rate will be calculated by the formula: <a href="https://msdn.microsoft.com/library/windows/hardware/ff554007">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a> value <b>vSyncFreq</b>  divided by the <b>DISPLAYCONFIG_VIDEO_SIGNAL_INFO</b> value <b>vSyncFreqDivider</b>. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff554007">DISPLAYCONFIG_VIDEO_SIGNAL_INFO</a>  value <b>vSyncFreqDivider</b> cannot be zero</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | iddcx.h |