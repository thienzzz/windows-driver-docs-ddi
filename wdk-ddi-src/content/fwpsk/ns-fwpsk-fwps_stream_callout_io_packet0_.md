---
UID : NS:fwpsk.FWPS_STREAM_CALLOUT_IO_PACKET0_
title : FWPS_STREAM_CALLOUT_IO_PACKET0_
author : windows-driver-content
description : The FWPS_STREAM_CALLOUT_IO_PACKET0 structure describes the data passed by the filter engine to a callout's classifyFn callout function when filtering a data stream.Note  FWPS_STREAM_CALLOUT_IO_PACKET0 is a specific version of FWPS_STREAM_CALLOUT_IO_PACKET. See WFP Version-Independent Names and Targeting Specific Versions of Windows for more information.
old-location : netvista\fwps_stream_callout_io_packet0.htm
old-project : netvista
ms.assetid : 2c0539f0-116e-4344-9584-db7416d258e0
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FWPS_STREAM_CALLOUT_IO_PACKET0_, FWPS_STREAM_CALLOUT_IO_PACKET0
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FWPS_STREAM_CALLOUT_IO_PACKET0
req.alt-loc : fwpsk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : FWPS_STREAM_CALLOUT_IO_PACKET0
---

# FWPS_STREAM_CALLOUT_IO_PACKET0_ structure
The <b>FWPS_STREAM_CALLOUT_IO_PACKET0</b> structure describes the data passed by the filter engine to a
  callout's 
  <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function when filtering a
  data stream.

## Syntax
````
typedef struct FWPS_STREAM_CALLOUT_IO_PACKET0_ {
  FWPS_STREAM_DATA0       *streamData;
  SIZE_T                  missedBytes;
  UINT32                  countBytesRequired;
  SIZE_T                  countBytesEnforced;
  FWPS_STREAM_ACTION_TYPE streamAction;
} FWPS_STREAM_CALLOUT_IO_PACKET0;
````

## Members

        
            `countBytesEnforced`

            A value set by a callout's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function. This value
     specifies the number of leading bytes of data in the portion of the data stream being processed to which
     the action specified by the 
     <b>streamAction</b> member or by the action returned by the callout function applies. Any remaining data
     in the stream buffer will be passed to the callout driver again the next time the filter engine calls
     the callout driver's 
     classifyFn callout function.
        
            `countBytesRequired`

            A value set by a callout's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function. This value
     specifies how many additional bytes of stream data are required by the callout function if it sets the 
     <b>streamAction</b> member to <b>FWPS_STREAM_ACTION_NEED_MORE_DATA</b>. The filter engine waits until it
     receives at least this many additional bytes of stream data before calling the callout driver's 
     classifyFn callout function again.
     

If a callout's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function sets the 
     <b>streamAction</b> member to a value other than <b>FWPS_STREAM_ACTION_NEED_MORE_DATA</b>, then it should set
     this member to zero.
        
            `missedBytes`

            The number of bytes in the data stream that are missing since the last time the callout driver's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function was called. This
     member is nonzero if a higher weight filter in the filter engine prevented the callout driver's 
     classifyFn callout function from processing a
     portion of the data stream.
        
            `streamAction`

            An <b>FWPS_STREAM_ACTION_TYPE</b> value set by a callout's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function that specifies
     the action to be applied to the data stream. This action is independent of the action returned by the
     callout function. A callout's 
     classifyFn callout function sets this member
     to one of the following:
        
            `streamData`

            A pointer to an 
     <a href="..\fwpsk\ns-fwpsk-fwps_stream_data0_.md">FWPS_STREAM_DATA0</a> structure that
     describes the portion of the data stream available to the callout driver's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function for processing.

    ## Remarks
        The filter engine passes a pointer to an <b>FWPS_STREAM_CALLOUT_IO_PACKET0</b> structure to a callout's 
    <a href="..\fwpsk\nc-fwpsk-fwps_callout_classify_fn0.md">classifyFn</a> callout function as the 
    <i>layerData</i> parameter when filtering a data stream.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
</dt>
<dt>
<a href="..\fwpsk\ns-fwpsk-fwps_stream_data0_.md">FWPS_STREAM_DATA0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpsstreamcontinue0.md">FwpsStreamContinue0</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/d9539403-7657-4e95-8791-309673d1207d">Types of Callouts</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_STREAM_CALLOUT_IO_PACKET0 structure%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>