---
UID : NS:pepfx._PEP_PPM_PARK_MASK
title : _PEP_PPM_PARK_MASK
author : windows-driver-content
description : The PEP_PROCESSOR_PARK_MASK structure contains the current core parking mask.
old-location : kernel\pep_ppm_park_mask.htm
old-project : kernel
ms.assetid : 528576FD-BDB2-4772-9151-A1C855BA953E
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _PEP_PPM_PARK_MASK, PEP_PPM_PARK_MASK, *PPEP_PPM_PARK_MASK
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : pepfx.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Supported starting with Windows 10.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PEP_PPM_PARK_MASK
req.alt-loc : pepfx.h
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
req.typenames : PEP_PPM_PARK_MASK, *PPEP_PPM_PARK_MASK
---

# _PEP_PPM_PARK_MASK structure
The <b>PEP_PROCESSOR_PARK_MASK</b> structure contains the current core parking mask.

## Syntax
````
typedef struct _PEP_PPM_PARK_MASK {
  ULONG                                              Count;
  ULONGLONG                                          EvaluationTime;
  _Field_size_full_(Count) PPEP_PROCESSOR_PARK_STATE Processors;
} PEP_PPM_PARK_MASK, *PPEP_PPM_PARK_MASK;
````

## Members

        
            `Count`

            [in] Indicates the number of processors in the <b>Processors</b> array.
        
            `EvaluationTime`

            [in] The interrupt time of the performance check evaluation that initiated this notification.
        
            `Processors`

            [in/out] An array of processors in the core parking domain.


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
<a href="https://msdn.microsoft.com/library/windows/hardware/mt186768">PEP_NOTIFY_PPM_PARK_MASK notification</a>
</dt>
<dt>
<a href="..\pepfx\ns-pepfx-_pep_processor_park_state.md">PEP_PROCESSOR_PARK_STATE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_PPM_PARK_MASK structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>