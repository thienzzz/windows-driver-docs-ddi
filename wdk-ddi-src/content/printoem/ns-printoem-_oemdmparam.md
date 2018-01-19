---
UID : NS:printoem._OEMDMPARAM
title : _OEMDMPARAM
author : windows-driver-content
description : The OEMDMPARAM structure is used as an input parameter to the IPrintOemUI::DevMode, IPrintOemUni::DevMode, and IPrintOemPS::DevMode methods.
old-location : print\oemdmparam.htm
old-project : print
ms.assetid : 625980d1-47eb-4427-a9e8-967b1873bbd6
ms.author : windowsdriverdev
ms.date : 1/8/2018
ms.keywords : _OEMDMPARAM, OEMDMPARAM, *POEMDMPARAM
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : printoem.h
req.include-header : Printoem.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : OEMDMPARAM
req.alt-loc : printoem.h
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
req.typenames : OEMDMPARAM, *POEMDMPARAM
req.product : Windows 10 or later.
---

# _OEMDMPARAM structure
The OEMDMPARAM structure is used as an input parameter to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554167">IPrintOemUI::DevMode</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff554230">IPrintOemUni::DevMode</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff553205">IPrintOemPS::DevMode</a> methods.

## Syntax
````
typedef struct _OEMDMPARAM {
  DWORD    cbSize;
  PVOID    pdriverobj;
  HANDLE   hPrinter;
  HANDLE   hModule;
  PDEVMODE pPublicDMIn;
  PDEVMODE pPublicDMOut;
  PVOID    pOEMDMIn;
  PVOID    pOEMDMOut;
  DWORD    cbBufSize;
} OEMDMPARAM, *POEMDMPARAM;
````

## Members

        
            `cbBufSize`

            On input, contains the caller-supplied size of memory space pointed to by <b>pOEMDMOut</b>. (Not valid if the <b>DevMode</b> method's <i>dwMode</i> value is OEMDM_SIZE.)

On output, contains the method-supplied size of the current version of the private DEVMODEW section. (Only used if the <b>DevMode</b> method's <i>dwMode</i> value is OEMDM_SIZE.)
        
            `cbSize`

            Contains the size of the OEMDMPARAM structure. Supplied by the Unidrv or Pscript5 driver.
        
            `hModule`

            Handle to the user interface plug-in module. Supplied by the Unidrv or Pscript5 driver.
        
            `hPrinter`

            Handle to the printer device. Supplied by the Unidrv or Pscript5 driver.
        
            `pdriverobj`

            
        
            `pOEMDMIn`

            Pointer to a set of private DEVMODEW members. Supplied by the Unidrv or Pscript5 driver. (Valid if the <b>DevMode</b> method's <i>dwMode</i> value is OEMDM_CONVERT or OEMDM_MERGE.)
        
            `pOEMDMOut`

            Pointer to memory allocated to receive modified private DEVMODEW contents. Supplied by the Unidrv or Pscript5 driver. (Valid if the <b>DevMode</b> method's <i>dwMode</i> value is OEMDM_DEFAULT, OEMDM_CONVERT or OEMDM_MERGE.)
        
            `pPublicDMIn`

            Pointer to the printer device's public DEVMODEW structure. Supplied by the Unidrv or Pscript5 driver. (Valid if the <b>DevMode</b> method's <i>dwMode</i> value is OEMDM_DEFAULT, OEMDM_CONVERT, or OEMDM_MERGE.)
        
            `pPublicDMOut`

            Pointer to a location to receive public DEVMODEW structure contents. Supplied by the Unidrv or Pscript5 driver. (Valid if the <b>DevMode</b> method's <i>dwMode</i> value is OEMDM_CONVERT or OEMDM_MERGE.)

    ## Remarks
        For more information about the use of OEMDMPARAM structure members, see the description of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff554167">IPrintOemUI::DevMode</a> method.</p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | printoem.h (include Printoem.h) |