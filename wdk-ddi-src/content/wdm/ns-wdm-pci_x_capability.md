---
UID : NS:wdm.PCI_X_CAPABILITY
title : PCI_X_CAPABILITY
author : windows-driver-content
description : The PCI_X_CAPABILITY structure reports the contents of the command and status registers of a device that is compliant with the PCI-X Addendum to the PCI Local Bus Specification.
old-location : pci\pci_x_capability.htm
old-project : PCI
ms.assetid : b30ccf86-ae6d-484a-a3f2-8b38df26e995
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : PCI_X_CAPABILITY, PCI_X_CAPABILITY, *PPCI_X_CAPABILITY
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : wdm.h
req.include-header : Wdm.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PCI_X_CAPABILITY
req.alt-loc : wdm.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : PASSIVE_LEVEL (see Remarks section)
req.typenames : PCI_X_CAPABILITY, *PPCI_X_CAPABILITY
req.product : Windows 10 or later.
---

# PCI_X_CAPABILITY structure
The PCI_X_CAPABILITY structure reports the contents of the command and status registers of a device that is compliant with the <i>PCI-X Addendum to the PCI Local Bus Specification.</i>

## Syntax
````
typedef struct {
  PCI_CAPABILITIES_HEADER Header;
  union {
    struct {
      USHORT DataParityErrorRecoveryEnable  :1;
      USHORT EnableRelaxedOrdering  :1;
      USHORT MaxMemoryReadByteCount  :2;
      USHORT MaxOutstandingSplitTransactions  :3;
      USHORT Reserved  :9;
    } bits;
    USHORT AsUSHORT;
  } Command;
  union {
    struct {
      ULONG FunctionNumber;
      ULONG DeviceNumber;
      ULONG BusNumber;
      ULONG Device64Bit;
      ULONG Capable133MHz;
      ULONG SplitCompletionDiscarded;
      ULONG UnexpectedSplitCompletion;
      ULONG DeviceComplexity;
      ULONG DesignedMaxMemoryReadByteCount;
      ULONG DesignedMaxOutstandingSplitTransactions;
      ULONG DesignedMaxCumulativeReadSize;
      ULONG ReceivedSplitCompletionErrorMessage;
      ULONG CapablePCIX266;
      ULONG CapablePCIX533;
    } bits;
    ULONG  AsULONG;
  } Status;
} PCI_X_CAPABILITY, *PPCI_X_CAPABILITY;
````

## Members

        
            `Command`

            
        
            `Header`

            Contains a structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff537454">PCI_CAPABILITIES_HEADER</a> that identifies the capability and provides a link to the next capability description.
        
            `Status`

            


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wdm.h (include Wdm.h) |

    ## See Also

        <dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff537454">PCI_CAPABILITIES_HEADER</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [PCI\buses]:%20PCI_X_CAPABILITY structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>