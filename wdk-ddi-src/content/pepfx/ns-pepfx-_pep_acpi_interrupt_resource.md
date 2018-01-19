---
UID : NS:pepfx._PEP_ACPI_INTERRUPT_RESOURCE
title : _PEP_ACPI_INTERRUPT_RESOURCE
author : windows-driver-content
description : The PEP_ACPI_INTERRUPT_RESOURCE structure describes an ACPI interrupt resource.
old-location : kernel\pep_acpi_interrupt_resource.htm
old-project : kernel
ms.assetid : B440AB0E-72CC-40F1-B77E-C12C84124737
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _PEP_ACPI_INTERRUPT_RESOURCE, *PPEP_ACPI_INTERRUPT_RESOURCE, PEP_ACPI_INTERRUPT_RESOURCE
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
req.alt-api : PEP_ACPI_INTERRUPT_RESOURCE
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
req.typenames : "*PPEP_ACPI_INTERRUPT_RESOURCE, PEP_ACPI_INTERRUPT_RESOURCE"
---

# _PEP_ACPI_INTERRUPT_RESOURCE structure
The <b>PEP_ACPI_INTERRUPT_RESOURCE</b> structure describes an ACPI interrupt resource.

## Syntax
````
typedef struct _PEP_ACPI_INTERRUPT_RESOURCE {
  PEP_ACPI_RESOURCE_TYPE  Type;
  KINTERRUPT_MODE         InterruptType;
  KINTERRUPT_POLARITY     InterruptPolarity;
  PEP_ACPI_RESOURCE_FLAGS Flags;
  UCHAR                   Count;
  PULONG                  Pins;
} PEP_ACPI_INTERRUPT_RESOURCE, *PPEP_ACPI_INTERRUPT_RESOURCE;
````

## Members

        
            `Count`

            The count of items in the <b>Pins</b> array.
        
            `Flags`

            A <a href="..\pepfx\ns-pepfx-_pep_acpi_resource_flags.md">PEP_ACPI_RESOURCE_FLAGS</a> structure that describes the capabilities of this ACPI resource.
        
            `InterruptPolarity`

            A <a href="..\wdm\ne-wdm-_kinterrupt_polarity.md">KINTERRUPT_POLARITY</a> enumeration value that identifies how a device signals an interrupt request on an interrupt line.
        
            `InterruptType`

            A <a href="..\wdm\ne-wdm-_kinterrupt_mode.md">KINTERRUPT_MODE</a> enumeration value that identifies the interrupt type.
        
            `Pins`

            A list of pin numbers on the resource that are described by this descriptor.
        
            `Type`

            A <a href="..\pepfx\ne-pepfx-_pep_acpi_resource_type.md">PEP_ACPI_RESOURCE_TYPE</a> enumeration value describing this resource.


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
<a href="..\pepfx\ne-pepfx-_pep_acpi_resource_type.md">PEP_ACPI_RESOURCE_TYPE</a>
</dt>
<dt>
<a href="..\wdm\ne-wdm-_kinterrupt_mode.md">KINTERRUPT_MODE</a>
</dt>
<dt>
<a href="..\wdm\ne-wdm-_kinterrupt_polarity.md">KINTERRUPT_POLARITY</a>
</dt>
<dt>
<a href="..\pepfx\ns-pepfx-_pep_acpi_resource_flags.md">PEP_ACPI_RESOURCE_FLAGS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20PEP_ACPI_INTERRUPT_RESOURCE structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>