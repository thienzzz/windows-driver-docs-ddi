---
UID : NF:bdasup.BdaCreateFilterFactoryEx
title : BdaCreateFilterFactoryEx function
author : windows-driver-content
description : The BdaCreateFilterFactoryEx function adds the specified filter descriptor as a filter factory to the specified device and associates the filter factory with the specified BDA template topology.
old-location : stream\bdacreatefilterfactoryex.htm
old-project : stream
ms.assetid : 105b6a66-5800-4079-af88-f44d01134ff0
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : BdaCreateFilterFactoryEx
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : bdasup.h
req.include-header : Bdasup.h
req.target-type : Desktop
req.target-min-winverclnt : Available on Microsoft Windows XP and later operating systems. This routine is available on the Windows 2000 platform only if Microsoft DirectX 9.0 and later is installed on that platform.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : BdaCreateFilterFactoryEx
req.alt-loc : Bdasup.lib,Bdasup.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Bdasup.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : KSP_BDA_NODE_PIN, *PKSP_BDA_NODE_PIN
---


# BdaCreateFilterFactoryEx function
The <b>BdaCreateFilterFactoryEx</b> function adds the specified filter descriptor as a filter factory to the specified device and associates the filter factory with the specified BDA template topology.

## Syntax

````
NTSTATUS BdaCreateFilterFactoryEx(
  _In_            PKSDEVICE           pKSDevice,
  _In_      const KSFILTER_DESCRIPTOR *pFilterDescriptor,
  _In_      const BDA_FILTER_TEMPLATE *pBdaFilterTemplate,
  _Out_opt_       PKSFILTERFACTORY    *ppKSFilterFactory
);
````

## Parameters

`pKSDevice`

Points to the BDA device to which to add the filter factory with associated BDA template topology.

`pFilterDescriptor`

Points to a <a href="..\ks\ns-ks-_ksfilter_descriptor.md">KSFILTER_DESCRIPTOR</a> structure that describes a filter for the BDA device. Note that not all of the template pin and node types may be exposed as pin and node factories when the filter is first initialized.

`pBdaFilterTemplate`

Points to a <a href="..\bdasup\ns-bdasup-_bda_filter_template.md">BDA_FILTER_TEMPLATE</a> structure that describes a BDA template topology.

`ppKSFilterFactory`

Points to a buffer that receives a pointer to a <a href="..\ks\ns-ks-_ksfilterfactory.md">KSFILTERFACTORY</a> structure for the newly created filter factory.


## Return Value

Returns STATUS_SUCCESS or an appropriate error code.

## Remarks

A BDA minidriver calls the <b>BdaCreateFilterFactoryEx</b> function to add a filter factory with an associated BDA template topology to a device and to register all of the topology's static template structures with the BDA support library (<i>BdaSup.sys</i>). The BDA support library can then handle the following method and property calls: 


<a href="https://msdn.microsoft.com/library/windows/hardware/ff563403">KSMETHODSETID_BdaChangeSync</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563404">KSMETHODSETID_BdaDeviceConfiguration</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566561">KSPROPSETID_BdaTopology</a>


A BDA minidriver calls <b>BdaCreateFilterFactoryEx</b> rather than the <a href="..\bdasup\nf-bdasup-bdacreatefilterfactory.md">BdaCreateFilterFactory</a> function whenever it requires a pointer to the newly created KSFILTERFACTORY. The <b>BdaCreateFilterFactory</b> function also creates a filter factory but doesn't return it to the caller. The BDA minidriver requires a pointer to the newly created KSFILTERFACTORY if the minidriver must call the <a href="..\ks\nf-ks-_ksedit.md">_KsEdit</a> function to edit KSFILTERFACTORY.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | bdasup.h (include Bdasup.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\bdasup\nf-bdasup-bdacreatefilterfactory.md">BdaCreateFilterFactory</a>
</dt>
<dt>
<a href="..\bdasup\ns-bdasup-_bda_filter_template.md">BDA_FILTER_TEMPLATE</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksdevice.md">KSDEVICE</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksfilter_descriptor.md">KSFILTER_DESCRIPTOR</a>
</dt>
<dt>
<a href="..\ks\nf-ks-_ksedit.md">_KsEdit</a>
</dt>
<dt>
<a href="..\ks\ns-ks-_ksfilterfactory.md">KSFILTERFACTORY</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563403">KSMETHODSETID_BdaChangeSync</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563404">KSMETHODSETID_BdaDeviceConfiguration</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566561">KSPROPSETID_BdaTopology</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20BdaCreateFilterFactoryEx function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>