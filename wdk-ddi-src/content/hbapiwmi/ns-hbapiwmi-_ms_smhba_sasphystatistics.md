---
UID : NS:hbapiwmi._MS_SMHBA_SASPHYSTATISTICS
title : _MS_SMHBA_SASPHYSTATISTICS
author : windows-driver-content
description : The MS_SMHBA_SASPHYSTATISTICS structure reports the traffic statistics for a SAS physical link.
old-location : storage\ms_smhba_sasphystatistics.htm
old-project : storage
ms.assetid : bb2ab242-9002-4760-86b2-1aaf203ff710
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _MS_SMHBA_SASPHYSTATISTICS, *PMS_SMHBA_SASPHYSTATISTICS, MS_SMHBA_SASPHYSTATISTICS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : hbapiwmi.h
req.include-header : Hbapiwmi.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : MS_SMHBA_SASPHYSTATISTICS
req.alt-loc : hbapiwmi.h
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
req.typenames : "*PMS_SMHBA_SASPHYSTATISTICS, MS_SMHBA_SASPHYSTATISTICS"
---

# _MS_SMHBA_SASPHYSTATISTICS structure
The MS_SMHBA_SASPHYSTATISTICS structure reports the traffic statistics for a SAS physical link.

## Syntax
````
typedef struct _MS_SMHBA_SASPHYSTATISTICS {
  LONGLONG SecondsSinceLastReset;
  LONGLONG TxFrames;
  LONGLONG TxWords;
  LONGLONG RxFrames;
  LONGLONG RxWords;
  LONGLONG InvalidDwordCount;
  LONGLONG RunningDisparityErrorCount;
  LONGLONG LossofDwordSyncCount;
  LONGLONG PhyResetProblemCount;
} MS_SMHBA_SASPHYSTATISTICS, *PMS_SMHBA_SASPHYSTATISTICS;
````

## Members

        
            `InvalidDwordCount`

            The number of invalid DWORDs.
        
            `LossofDwordSyncCount`

            The loss of synchronization count.
        
            `PhyResetProblemCount`

            A count of the number of physical link reset problems.
        
            `RunningDisparityErrorCount`

            The number of disparity error counts.
        
            `RxFrames`

            The number of received SAS frames across all protocols and classes.
        
            `RxWords`

            The number of received SAS words across all protocols and classes.
        
            `SecondsSinceLastReset`

            The number of seconds since the statistics were last reset.
        
            `TxFrames`

            The number of transmitted SAS frames across all protocols and classes.
        
            `TxWords`

            The number of transmitted SAS words across all protocols and classes.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | hbapiwmi.h (include Hbapiwmi.h) |