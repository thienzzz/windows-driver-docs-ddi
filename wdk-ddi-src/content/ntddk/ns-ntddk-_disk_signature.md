---
UID : NS:ntddk._DISK_SIGNATURE
title : _DISK_SIGNATURE
author : windows-driver-content
description : DISK_SIGNATURE contains the disk signature information for a disk's partition table.
old-location : storage\disk_signature.htm
old-project : storage
ms.assetid : f3fdb436-53b6-4fb3-8746-1f852f7d928a
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _DISK_SIGNATURE, DISK_SIGNATURE, *PDISK_SIGNATURE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddk.h
req.include-header : Ntddk.h
req.target-type : Windows
req.target-min-winverclnt : This structure is only available on Windows XP and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DISK_SIGNATURE
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
req.irql : PASSIVE_LEVEL
req.typenames : DISK_SIGNATURE, *PDISK_SIGNATURE
---

# _DISK_SIGNATURE structure
DISK_SIGNATURE contains the disk signature information for a disk's partition table.

## Syntax
````
typedef struct _DISK_SIGNATURE {
  ULONG PartitionStyle;
  union {
    struct {
      ULONG Signature;
      ULONG CheckSum;
    } Mbr;
    struct {
      GUID DiskId;
    } Gpt;
  };
} DISK_SIGNATURE, *PDISK_SIGNATURE;
````

## Members

        
            `PartitionStyle`

            Specifies the type of partition.  See <a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a> for a description of the possible values.


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
<a href="..\ntddk\nf-ntddk-ioreaddisksignature.md">IoReadDiskSignature</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20DISK_SIGNATURE structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>