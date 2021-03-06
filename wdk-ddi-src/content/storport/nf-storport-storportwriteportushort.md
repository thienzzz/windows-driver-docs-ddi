---
UID: NF:storport.StorPortWritePortUshort
title: StorPortWritePortUshort macro
author: windows-driver-content
description: The StorPortWritePortUshort routine writes a value to a specified register address.
old-location: storage\storportwriteportushort.htm
old-project: storage
ms.assetid: 7655b6a1-2ed4-4e57-b8b5-e7b8ff2dd1e5
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: StorPortWritePortUshort, StorPortWritePortUshort routine [Storage Devices], storage.storportwriteportushort, storport/StorPortWritePortUshort, storprt_7e675f67-f027-48e7-a41b-b672b0f81d20.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Storport.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Storport.lib
-	Storport.dll
api_name:
-	StorPortWritePortUshort
product:
- Windows
targetos: Windows
req.typenames: 
---

# StorPortWritePortUshort macro


## -description


The <b>StorPortWritePortUshort</b> routine writes a value to a specified register address. 


## -parameters




### -param h

TBD


### -param p

TBD


### -param v

TBD






#### - HwDeviceExtension [in]

Pointer to the hardware device extension.


#### - Port [in]

Contains the address of the port to be written to. 


#### - Value [in]

Contains the value to be written. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff564841">ScsiPortWritePortUshort</a>. For a buffered equivalent of this routine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff567520">StorPortWritePortBufferUshort</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564841">ScsiPortWritePortUshort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567520">StorPortWritePortBufferUshort</a>
 

 

