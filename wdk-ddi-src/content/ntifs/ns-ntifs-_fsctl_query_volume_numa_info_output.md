---
UID : NS:ntifs._FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT
title : _FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT
author : windows-driver-content
description : The FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT structure specifies the Non-Uniform Memory Architecture (NUMA) node the volume resides on.
old-location : ifsk\fsctl_query_volume_numa_info_output_.htm
old-project : ifsk
ms.assetid : 3BB6F409-A716-4990-B1C6-D0F8035DA7F0
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : _FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT, FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT, *PFSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntifs.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT
req.alt-loc : Ntifs.h
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
req.typenames : FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT, *PFSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT
---

# _FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT structure
The <b>FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT</b> structure specifies the Non-Uniform Memory Architecture (NUMA) node the volume resides on.

## Syntax
````
typedef struct _FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT  {
  ULONG NumaNode;
} FSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT , *PFSCTL_QUERY_VOLUME_NUMA_INFO_OUTPUT ;
````

## Members

        
            `NumaNode`

            Specifies the number of the NUMA node the volume resides on.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h |