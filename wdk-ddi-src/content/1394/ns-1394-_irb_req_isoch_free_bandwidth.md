---
UID : NS:1394._IRB_REQ_ISOCH_FREE_BANDWIDTH
title : _IRB_REQ_ISOCH_FREE_BANDWIDTH
author : windows-driver-content
description : This structure contains the fields necessary in order for the Bus driver to carry out an IsochFreeBandwidth request.
old-location : ieee\irb_req_isoch_free_bandwidth.htm
old-project : IEEE
ms.assetid : 1401F3B5-4F3F-47C1-88F9-96AFCCF2AA7E
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _IRB_REQ_ISOCH_FREE_BANDWIDTH, IRB_REQ_ISOCH_FREE_BANDWIDTH
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : 1394.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IRB_REQ_ISOCH_FREE_BANDWIDTH
req.alt-loc : 1394.h
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
req.typenames : IRB_REQ_ISOCH_FREE_BANDWIDTH
---

# _IRB_REQ_ISOCH_FREE_BANDWIDTH structure
This structure contains the fields necessary in order for the Bus driver to carry out an <b>IsochFreeBandwidth</b> request.

## Syntax
````
typedef struct _IRB_REQ_ISOCH_FREE_BANDWIDTH {
  HANDLE hBandwidth;
} IRB_REQ_ISOCH_FREE_BANDWIDTH;
````

## Members

        
            `hBandwidth`

            Specifies the bandwidth handle to release.

    ## Remarks
        If successful, the bus driver sets <b>Irp-&gt;IoStatus.Status</b> to STATUS_SUCCESS, and the isochronous bandwidth is returned to the pool of available bandwidth.

A status of STATUS_INVALID_GENERATION also indicates success. 

Do not resend the REQUEST_ISOCH_FREE_BANDWIDTH request in order to release isochronous bandwidth if the request failed with the STATUS_INVALID_GENERATION error code. In that case, it is safe to assume that isochronous bandwidth was released as a result of 1394 bus generation changes.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | 1394.h |