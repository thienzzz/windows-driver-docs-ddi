---
UID : NS:smclib._SCARD_READER_CAPABILITIES
title : _SCARD_READER_CAPABILITIES
author : windows-driver-content
description : The SCARD_READER_CAPABILITIES structure holds state information about the smart card reader.
old-location : smartcrd\scard_reader_capabilities.htm
old-project : smartcrd
ms.assetid : f55b74d0-d545-419a-87fb-c320f789aaf4
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : _SCARD_READER_CAPABILITIES, SCARD_READER_CAPABILITIES, *PSCARD_READER_CAPABILITIES
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : smclib.h
req.include-header : Smclib.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : SCARD_READER_CAPABILITIES
req.alt-loc : Smclib.h
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
req.typenames : SCARD_READER_CAPABILITIES, *PSCARD_READER_CAPABILITIES
req.product : Windows 10 or later.
---

# _SCARD_READER_CAPABILITIES structure
The SCARD_READER_CAPABILITIES structure holds state information about the smart card reader.

## Syntax
````
typedef struct {
  ULONG  SupportedProtocols;
  ULONG  ReaderType;
  ULONG  Reserved;
  ULONG  MechProperties;
  ULONG  CurrentState;
  ULONG  Channel;
  struct {
    ULONG Default;
    ULONG Max;
  } CLKFrequency;
  struct {
    ULONG Default;
    ULONG Max;
  } DataRate;
  ULONG  MaxIFSD;
  ULONG  PowerMgmtSupport;
  ULONG  CardConfiscated;
  struct {
    PULONG List;
    UCHAR  Entries;
  } DataRatesSupported;
  struct {
    PULONG List;
    UCHAR  Entries;
  } CLKFrequenciesSupported;
  UCHAR  Reserved1[100 - sizeof(ULONG) -  sizeof(struct _DataRatesSupported) - sizeof(struct _CLKFrequenciesSupported)];
} SCARD_READER_CAPABILITIES, *PSCARD_READER_CAPABILITIES;
````

## Members

        
            `CardConfiscated`

            If <b>TRUE</b>, indicates that the smart card was confiscated.
        
            `Channel`

            Contains the logical channel number. This member is optional. The exact meaning of this member depends on the type of smart card, as shown in the following table. 

<table>
<tr>
<th>Type of smart card</th>
<th>Meaning of value in channel field</th>
</tr>
<tr>
<td>
Serial reader

</td>
<td>
Port number

</td>
</tr>
<tr>
<td>
Parallel reader

</td>
<td>
Port number

</td>
</tr>
<tr>
<td>
SCSI reader

</td>
<td>
SCSI ID

</td>
</tr>
<tr>
<td>
Keyboard reader

</td>
<td>
0

</td>
</tr>
<tr>
<td>
USB reader

</td>
<td>
Device number

</td>
</tr>
</table>
 

For more information, see Part 3 of the <i>Interoperability Specification for ICCs and Personal Computer Systems</i>.
        
            `CLKFrequenciesSupported`

            A structure with the following members:
        
            `CLKFrequency`

            A structure with the following members:
        
            `CurrentState`

            This member contains the status of the card and is required. This member can have one of the values listed in the following table.

<table>
<tr>
<th>Status</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SCARD_UNKNOWN

</td>
<td>
The reader does not have information about the status.

</td>
</tr>
<tr>
<td>
SCARD_ABSENT

</td>
<td>
No smart card is inserted.

</td>
</tr>
<tr>
<td>
SCARD_PRESENT

</td>
<td>
A smart card is inserted.

</td>
</tr>
<tr>
<td>
SCARD_SWALLOWED

</td>
<td>
A smart card is inserted and the reader has swallowed it.

</td>
</tr>
<tr>
<td>
SCARD_POWERED

</td>
<td>
The smart card is turned on, but the reader does not recognize its mode.

</td>
</tr>
<tr>
<td>
SCARD_NEGOTIABLE

</td>
<td>
A smart card is inserted and awaits protocol negotiation.

</td>
</tr>
<tr>
<td>
SCARD_SPECIFIC

</td>
<td>
A smart card is inserted and a protocol has been selected.

</td>
</tr>
</table>
 

Access to this field must be sequentialized by using the spin lock pointed to by the <b>OsData-&gt;SpinLock</b> member of <a href="..\smclib\ns-smclib-_smartcard_extension.md">SMARTCARD_EXTENSION</a>.
        
            `DataRate`

            A structure with the following members:
        
            `DataRatesSupported`

            A structure with the following members:
        
            `MaxIFSD`

            Contains the maximum buffer size of the reader. This value informs the smart card at the beginning of a T=1 transmission of the maximum number of bytes that can be received in one packet. This member is required.
        
            `MechProperties`

            Contains a value that is formed by taking a bitwise OR of all applicable reader properties shown in the following table. This member is optional. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SCARD_READER_SWALLOWS

</td>
<td>
Reader has a swallowing mechanism.

</td>
</tr>
<tr>
<td>
SCARD_READER_EJECTS

</td>
<td>
Reader can eject the smart card.

</td>
</tr>
<tr>
<td>
SCARD_READER_CONFISCATES

</td>
<td>
Reader can swallow the smart card.

</td>
</tr>
</table>
        
            `PowerMgmtSupport`

            Indicates the type of power management that the card supports. A value of zero indicates that the smart card does not support power management.
        
            `ReaderType`

            This member contains the reader type and is required. This member can have one of the values in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SCARD_READER_TYPE_SERIAL

</td>
<td>
Serial reader

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_PCMCIA

</td>
<td>
PCMCIA reader

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_KEYBOARD

</td>
<td>
Keyboard-attached reader

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_USB

</td>
<td>
USB reader

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_PARALELL

</td>
<td>
Parallel reader 

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_SCSI

</td>
<td>
SCSI reader 

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_IDE

</td>
<td>
IDE reader 

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_TPM

</td>
<td>
Reader that uses a TPM chip for key material storage and cryptographic operations

</td>
</tr>
<tr>
<td>
SCARD_READER_TYPE_VENDOR

</td>
<td>
Reader that uses a proprietary vendor bus 

</td>
</tr>
</table>
        
            `Reserved`

            Reserved for system use.
        
            `Reserved1`

            Reserved for system use.
        
            `SupportedProtocols`

            Must be set to a bitmask that reflects the asynchronous or synchronous protocols that the card reader and card reader driver support. This member is required.

    ## Remarks
        This structure must be maintained by the smart card reader driver. </p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | smclib.h (include Smclib.h) |