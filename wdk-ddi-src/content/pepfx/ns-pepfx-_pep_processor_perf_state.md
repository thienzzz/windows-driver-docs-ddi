---
UID : NS:pepfx._PEP_PROCESSOR_PERF_STATE
title : _PEP_PROCESSOR_PERF_STATE
author : windows-driver-content
description : Use in the PEP_NOTIFY_PPM_QUERY_DISCRETE_PERF_STATES  notification. This structure describes the properties of a single performance state.  .
old-location : kernel\pep_processor_perf_state.htm
old-project : kernel
ms.assetid : 46231ac0-2c34-4154-8b3e-f34c40cbff4a
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _PEP_PROCESSOR_PERF_STATE, PEP_PROCESSOR_PERF_STATE, *PPEP_PROCESSOR_PERF_STATE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : pepfx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Windows 10, version 1709
req.target-min-winversvr : Windows Server 2016
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PEP_PROCESSOR_PERF_STATE
req.alt-loc : Pepfx.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : PEP_PROCESSOR_PERF_STATE, *PPEP_PROCESSOR_PERF_STATE
---

# _PEP_PROCESSOR_PERF_STATE structure
Use in the <b>PEP_NOTIFY_PPM_QUERY_DISCRETE_PERF_STATES</b>  notification. This structure describes the properties of a single performance state.

## Syntax
````
typedef struct _PEP_PROCESSOR_PERF_STATE {
  ULONG     Performance;
  ULONG     Frequency;
  ULONG [4] Reserved;
} PEP_PROCESSOR_PERF_STATE, PEP_PROCESSOR_PERF_STATE;
````

## Members

        
            `Frequency`

            On output, the frequency (in MHz) of this performance state.
        
            `Performance`

            On output, the performance level (on the scale returned by the <a href="..\pepfx\ns-pepfx-_pep_query_component_perf_capabilities.md">PEP_QUERY_COMPONENT_PERF_CAPABILITIES</a> notification) of this performance state.
        
            `Reserved`

            Reserved.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | pepfx.h |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/506b3d8e-4aba-4e70-a6db-52a52d717c6b">PEP_PPM_QUERY_DISCRETE_PERF_STATES</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt186881">Processor power management (PPM) notifications</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_PROCESSOR_PERF_STATE structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>