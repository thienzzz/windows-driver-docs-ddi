---
UID : NE:ntddk._WHEA_ERROR_SOURCE_TYPE
title : _WHEA_ERROR_SOURCE_TYPE
author : windows-driver-content
description : The WHEA_ERROR_SOURCE_TYPE enumeration defines the different types of error sources that can report hardware errors.
old-location : whea\whea_error_source_type.htm
old-project : whea
ms.assetid : d2615320-6c8a-4813-afb5-c5b510e5fde9
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _WHEA_ERROR_SOURCE_TYPE, *PWHEA_ERROR_SOURCE_TYPE, WHEA_ERROR_SOURCE_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Windows
req.target-min-winverclnt : Supported in Windows Server 2008, Windows Vista SP1, and later versions of Windows.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WHEA_ERROR_SOURCE_TYPE
req.alt-loc : ntddk.h
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
req.typenames : "*PWHEA_ERROR_SOURCE_TYPE, WHEA_ERROR_SOURCE_TYPE"
---

# _WHEA_ERROR_SOURCE_TYPE Enumeration
The WHEA_ERROR_SOURCE_TYPE enumeration defines the different types of error sources that can report hardware errors.

## Syntax
````
typedef enum _WHEA_ERROR_SOURCE_TYPE { 
  WheaErrSrcTypeMCE         = 0x00,
  WheaErrSrcTypeCMC         = 0x01,
  WheaErrSrcTypeCPE         = 0x02,
  WheaErrSrcTypeNMI         = 0x03,
  WheaErrSrcTypePCIe        = 0x04,
  WheaErrSrcTypeGeneric     = 0x05,
  WheaErrSrcTypeINIT        = 0x06,
  WheaErrSrcTypeBOOT        = 0x07,
  WheaErrSrcTypeSCIGeneric  = 0x08,
  WheaErrSrcTypeIPFMCA      = 0x09,
  WheaErrSrcTypeIPFCMC      = 0x0a,
  WheaErrSrcTypeIPFCPE      = 0x0b,
  WheaErrSrcTypeMax
} WHEA_ERROR_SOURCE_TYPE, *PWHEA_ERROR_SOURCE_TYPE;
````

## Constants

<table>

<tr>
<td>WheaErrSrcTypeBOOT</td>
<td>A boot error source.</td>
</tr>

<tr>
<td>WheaErrSrcTypeCMC</td>
<td>A corrected machine check (CMC).</td>
</tr>

<tr>
<td>WheaErrSrcTypeCPE</td>
<td>A corrected platform error (CPE).</td>
</tr>

<tr>
<td>WheaErrSrcTypeGeneric</td>
<td>A type of error source that does not conform to any of the other WHEA_ERROR_SOURCE_TYPE enumeration values.</td>
</tr>

<tr>
<td>WheaErrSrcTypeINIT</td>
<td>An Itanium processor INIT error.</td>
</tr>

<tr>
<td>WheaErrSrcTypeIPFCMC</td>
<td>An Itanium processor corrected machine check (CMC).</td>
</tr>

<tr>
<td>WheaErrSrcTypeIPFCPE</td>
<td>An Itanium processor corrected platform error (CPE).</td>
</tr>

<tr>
<td>WheaErrSrcTypeIPFMCA</td>
<td>An Itanium processor machine check abort (MCA).</td>
</tr>

<tr>
<td>WheaErrSrcTypeMax</td>
<td>The maximum number of error source types that can report hardware errors.</td>
</tr>

<tr>
<td>WheaErrSrcTypeMCE</td>
<td>A machine check exception (MCE).</td>
</tr>

<tr>
<td>WheaErrSrcTypeNMI</td>
<td>A nonmaskable interrupt (NMI).</td>
</tr>

<tr>
<td>WheaErrSrcTypePCIe</td>
<td>A PCI Express (PCIe) error.</td>
</tr>

<tr>
<td>WheaErrSrcTypeSCIGeneric</td>
<td>A service control interrupt (SCI).</td>
</tr>
</table>

## Remarks

The <a href="..\ntddk\ns-ntddk-_whea_error_source_descriptor.md">WHEA_ERROR_SOURCE_DESCRIPTOR</a> structure contains a member of type WHEA_ERROR_SOURCE_TYPE that specifies the type of error source that is described by the structure.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560465">WHEA_ERROR_PACKET</a> structure contains a member of type WHEA_ERROR_SOURCE_TYPE that specifies the type of error source that caused the error condition described by the structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h) |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560465">WHEA_ERROR_PACKET</a>
</dt>
<dt>
<a href="..\ntddk\ns-ntddk-_whea_error_source_descriptor.md">WHEA_ERROR_SOURCE_DESCRIPTOR</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [whea\whea]:%20WHEA_ERROR_SOURCE_TYPE enumeration%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>