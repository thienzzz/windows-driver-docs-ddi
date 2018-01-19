---
UID : NS:ks._KSDEVICE_DESCRIPTOR
title : _KSDEVICE_DESCRIPTOR
author : windows-driver-content
description : The KSDEVICE_DESCRIPTOR structure describes the characteristics of a particular device.
old-location : stream\ksdevice_descriptor.htm
old-project : stream
ms.assetid : dc68f6d8-a2d5-4940-a708-fe761c3a8a0d
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : _KSDEVICE_DESCRIPTOR, *PKSDEVICE_DESCRIPTOR, KSDEVICE_DESCRIPTOR
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ks.h
req.include-header : Ks.h
req.target-type : Windows
req.target-min-winverclnt : Available in Microsoft Windows XP and later operating systems and in Microsoft DirectX 8.0 and later versions.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KSDEVICE_DESCRIPTOR
req.alt-loc : ks.h
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
req.typenames : "*PKSDEVICE_DESCRIPTOR, KSDEVICE_DESCRIPTOR"
---

# _KSDEVICE_DESCRIPTOR structure
The KSDEVICE_DESCRIPTOR structure describes the characteristics of a particular device.

## Syntax
````
typedef struct _KSDEVICE_DESCRIPTOR {
  const KSDEVICE_DISPATCH   *Dispatch;
  ULONG                     FilterDescriptorsCount;
  const KSFILTER_DESCRIPTOR *FilterDescriptors;
  ULONG                     Version;
  ULONG                     Flags;
} KSDEVICE_DESCRIPTOR, *PKSDEVICE_DESCRIPTOR;
````

## Members


    ## Remarks
        Most often, this structure is used in conjunction with <a href="..\ks\nf-ks-ksinitializedriver.md">KsInitializeDriver</a> in the client's <b>DriverEntry</b> function to initialize the device. This structure is also used to manually initialize or create devices with the <a href="..\ks\nf-ks-ksinitializedevice.md">KsInitializeDevice</a> and <a href="..\ks\nf-ks-kscreatedevice.md">KsCreateDevice</a> functions.

If you set <b>Version</b> to KSDEVICE_DESCRIPTOR_VERSION_2 and run your driver on an early version of AVStream that does not support <b>Flags</b>, all flags will be considered to be zero.

Similarly, using an earlier version descriptor on later versions of AVStream causes no flags to be specified.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ks.h (include Ks.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ks\ns-ks-_ksdevice_dispatch.md">KSDEVICE_DISPATCH</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksfilter_descriptor.md">KSFILTER_DESCRIPTOR</a>
</dt>
<dt>
<a href="..\ks\nf-ks-ksinitializedriver.md">KsInitializeDriver</a>
</dt>
<dt>
<a href="..\ks\nf-ks-ksinitializedevice.md">KsInitializeDevice</a>
</dt>
<dt>
<a href="..\ks\nf-ks-kscreatedevice.md">KsCreateDevice</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSDEVICE_DESCRIPTOR structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>