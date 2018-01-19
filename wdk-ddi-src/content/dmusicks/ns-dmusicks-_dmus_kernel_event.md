---
UID : NS:dmusicks._DMUS_KERNEL_EVENT
title : _DMUS_KERNEL_EVENT
author : windows-driver-content
description : The DMUS_KERNEL_EVENT structure is used to package time-stamped music events.
old-location : audio\dmus_kernel_event.htm
old-project : audio
ms.assetid : 652f64e2-310b-46c9-8b00-c827a7475b07
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _DMUS_KERNEL_EVENT, DMUS_KERNEL_EVENT, *PDMUS_KERNEL_EVENT
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : dmusicks.h
req.include-header : Dmusicks.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DMUS_KERNEL_EVENT
req.alt-loc : dmusicks.h
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
req.typenames : DMUS_KERNEL_EVENT, *PDMUS_KERNEL_EVENT
---

# _DMUS_KERNEL_EVENT structure
The DMUS_KERNEL_EVENT structure is used to package time-stamped music events.

## Syntax
````
typedef struct _DMUS_KERNEL_EVENT {
  BYTE               bReserved;
  BYTE               cbStruct;
  USHORT             cbEvent;
  USHORT             usChannelGroup;
  USHORT             usFlags;
  REFERENCE_TIME     ullPresTime100ns;
  ULONGLONG          ullBytePosition;
  _DMUS_KERNEL_EVENT *pNextEvt;
  union {
    BYTE               abData[sizeof(PBYTE)];
    PBYTE              pbData;
    _DMUS_KERNEL_EVENT *pPackageEvt;
  } uData;
} DMUS_KERNEL_EVENT, *PDMUS_KERNEL_EVENT;
````

## Members

        
            `bReserved`

            Miniport drivers should not modify this member. Reserved for future use. Do not use.
        
            `cbEvent`

            Specifies the unrounded number of event bytes referred to by <b>uData</b>.
        
            `cbStruct`

            Miniport drivers should not modify this member.
       This member specifies the size of the DMUS_KERNEL_EVENT structure itself and could change in the future.
        
            `pNextEvt`

            Pointer to the next event in the list, or <b>NULL</b> if no event follows. This facilitates passing chains of identically time-stamped messages to the miniport driver. Additionally, hardware that does its own mixing can receive or transmit groups of messages at one time.
        
            `uData`

            
        
            `ullBytePosition`

            8 16
        
            `ullPresTime100ns`

            Specifies the presentation time for this event. This 64-bit value is expressed in 100-nanosecond units. The master clock should be used to evaluate this presentation time.
        
            `usChannelGroup`

            Specifies which channel group (set of 16 MIDI channels) receives or originated this event. This is unique only within the target MIDI device (miniport driver).
        
            `usFlags`

            Specifies whether an event is a package and whether this event concludes the message. A package encapsulates a list of events that should be dealt with atomically. This member is a bitfield that can be set to the bitwise OR of one or more of the following flag bits:

    ## Remarks
        The DMUS_KERNEL_EVENT structure is used by WDM audio drivers that provide kernel streaming support for DirectMusic.

While capturing a MIDI stream, the DMus port driver calls the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536494">IAllocatorMXF::GetMessage</a> method to retrieve DMUS_KERNEL_EVENT structures to hold the captured data. While rendering a MIDI stream, the port driver calls the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536791">IMXF::PutMessage</a> method to discard DMUS_KERNEL_EVENT structures as it finishes reading them. For more information, see <a href="https://msdn.microsoft.com/ce9ec589-0aea-4ed9-a60d-50f2ddfb0c13">MIDI Transport</a>.

In the case of MIDI capture, the DMUS_KERNEL_EVENT structure can be packaged with single, multiple, or fragmentary MIDI messages. The <b>usFlags</b> member should be set to DMUS_KEF_EVENT_INCOMPLETE unless it is a single complete MIDI message. This structure also contains:

A time stamp relative to the master clock (ullPresTime100Ns)

Extended channel information (usChannelGroup)

Mapping to the correct DLS instrument is implicit in the triplet of

&lt;<i>pin</i>, <i>channel_group</i>, <i>channel</i>&gt;

Presentation time does not advance during the states KSSTATE_PAUSE and KSSTATE_STOP, and is reset during KSSTATE_STOP. For more information, see <a href="https://msdn.microsoft.com/e3ffc7ca-f3cd-4989-af40-78b6a2438f95">KS Clocks</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dmusicks.h (include Dmusicks.h) |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536791">IMXF::PutMessage</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536494">IAllocatorMXF::GetMessage</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [audio\audio]:%20DMUS_KERNEL_EVENT structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>