---
UID : NS:iddcx.IDDCX_TARGET_MODE
title : IDDCX_TARGET_MODE
author : windows-driver-content
description : Gives information about the target mode signal, including the bandwidth needed for the mode.
old-location : display\iddcx_target_mode.htm
old-project : display
ms.assetid : 10bb23fa-ff1e-4bda-ba64-59a19da5f87e
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : IDDCX_TARGET_MODE,
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
req.alt-api : IDDCX_TARGET_MODE
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

# IDDCX_TARGET_MODE structure
Gives information about the target mode signal, including the bandwidth needed for the mode.

## Syntax
````
typedef struct IDDCX_TARGET_MODE {
  UINT                      Size;
  DISPLAYCONFIG_TARGET_MODE TargetVideoSignalInfo;
  UINT64                    RequiredBandwidth;
} IDDCX_TARGET_MODE, *IDDCX_TARGET_MODE;
````

## Members

        
            `RequiredBandwidth`

            The display pipeline bandwidth required for this mode.
        
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