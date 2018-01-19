---
UID : NS:compstui._COMPROPSHEETUI
title : _COMPROPSHEETUI
author : windows-driver-content
description : The COMPROPSHEETUI structure is used as an input parameter to CPSUI's ComPropSheet function, if the function code is CPSFUNC_ADD_PCOMPROPSHEETUI. All structure members must be supplied by the caller of ComPropSheet.
old-location : print\compropsheetui.htm
old-project : print
ms.assetid : 7ebf46b7-5c31-482e-8644-a3d81f7dc5cc
ms.author : windowsdriverdev
ms.date : 1/8/2018
ms.keywords : _COMPROPSHEETUI, COMPROPSHEETUI, *PCOMPROPSHEETUI
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : compstui.h
req.include-header : Compstui.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : COMPROPSHEETUI
req.alt-loc : compstui.h
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
req.typenames : COMPROPSHEETUI, *PCOMPROPSHEETUI
---

# _COMPROPSHEETUI structure
The COMPROPSHEETUI structure is used as an input parameter to CPSUI's <a href="https://msdn.microsoft.com/library/windows/hardware/ff546207">ComPropSheet</a> function, if the function code is <a href="https://msdn.microsoft.com/library/windows/hardware/ff546388">CPSFUNC_ADD_PCOMPROPSHEETUI</a>. All structure members must be supplied by the caller of <i>ComPropSheet</i>.

## Syntax
````
typedef struct _COMPROPSHEETUI {
  WORD           cbSize;
  WORD           Flags;
  HINSTANCE      hInstCaller;
  LPTSTR         pCallerName;
  ULONG_PTR      UserData;
  LPTSTR         pHelpFile;
  _CPSUICALLBACK pfnCallBack;
  POPTITEM       pOptItem;
  PDLGPAGE       pDlgPage;
  WORD           cOptItem;
  WORD           cDlgPage;
  ULONG_PTR      IconID;
  LPTSTR         pOptItemName;
  WORD           CallerVersion;
  WORD           OptItemVersion;
  ULONG_PTR      dwReserved[4];
} COMPROPSHEETUI, *PCOMPROPSHEETUI;
````

## Members

        
            `CallerVersion`

            Caller-supplied version number, representing the calling application's current version. The high byte identifies the major version, and the low byte is the minor version. For example, a <b>CallerVersion</b> value of 0x310 specifies a caller version number of 3.16. The version number is displayed when a user clicks on a page's <b>About</b> button.
        
            `cbSize`

            Caller-supplied size, in bytes, of the COMPROPSHEETUI structure.
        
            `cDlgPage`

            Caller-supplied number of <a href="..\compstui\ns-compstui-_dlgpage.md">DLGPAGE</a> structures pointed to by <b>pDlgPage</b>. Not used if <b>pDlgPage</b> specifies a predefined CPSUI_PDLGPAGE-prefixed structure.
        
            `cOptItem`

            Caller-supplied number of <a href="..\compstui\ns-compstui-_optitem.md">OPTITEM</a> structures pointed to by <b>pOptItem</b>.
        
            `dwReserved`

            Reserved. This array must be set to zero.
        
            `Flags`

            Optional caller-supplied bit flags, as described in the following list:
        
            `hInstCaller`

            Caller-supplied module instance handle, received by the DLL's entry point function.
        
            `IconID`

            Caller-supplied, can be one of the following:

<ul>
<li>
An icon resource identifier. This can be application-defined, or it can be one of the CPSUI-supplied, IDI_CPSUI-prefixed icon resource identifiers.

</li>
<li>
An icon handle. If a handle is specified, CPSUIF_ICONID_AS_HICON must be set in the <b>Flags</b> member.

</li>
</ul>
The specified icon is displayed in the root node of the property sheet page's treeview.
        
            `OptItemVersion`

            Caller-supplied version number, representing the root-level option item's current version. For printer interface DLLs, this typically represents a printer device version. The high byte identifies the major version, and the low byte is the minor version. For example, an <b>OptItemVersion</b> value of 0x3ff specifies a caller version number of 3.255. The version number is displayed when a user clicks on a page's <b>About</b> button.
        
            `pCallerName`

            Caller-supplied pointer to a NULL-terminated text string representing the application's name. (For a printer interface DLL, this should be the driver's name, such as "PostScript Driver".)
        
            `pDlgPage`

            This member specifies <a href="..\compstui\ns-compstui-_dlgpage.md">DLGPAGE</a> structures that describe pages to be added to the property sheet. It can be either of the following:

<ul>
<li>
A pointer to an array of DLGPAGE structures.

</li>
<li>
One of the pointers that is described in the following list. These pointers reference predefined DLGPAGE structures, supplied by CPSUI for use by printer interface DLLs.
        
            `pfnCallBack`

            Caller-supplied pointer to a <a href="..\compstui\nc-compstui-_cpsuicallback.md">_CPSUICALLBACK</a>-typed callback function, which CPSUI calls when a user modifies the page's option values.

Can be used only if <b>pDlgPage</b> identifies a CPSUI-supplied <a href="..\compstui\ns-compstui-_dlgpage.md">DLGPAGE</a> structure, or if the <b>DlgProc</b> member of an application-supplied DLGPAGE structure is <b>NULL</b>.
        
            `pHelpFile`

            Caller-supplied pointer to a NULL-terminated text string representing a path to a help file. For printer interface DLLs, this is typically the help file path obtained by calling GetPrinterDriver (described in the Microsoft Windows SDK documentation).

The help file is indexed by values contained in the <b>HelpIndex</b> member of <a href="..\compstui\ns-compstui-_optitem.md">OPTITEM</a> structures.
        
            `pOptItem`

            Caller-supplied pointer to an array of <a href="..\compstui\ns-compstui-_optitem.md">OPTITEM</a> structures describing the page's options.
        
            `pOptItemName`

            Caller-supplied pointer to a NULL-terminated string to be displayed in the root node of the property sheet page's treeview. For printer interface DLLs, this string typically represents a printer device type, such as "HP 4si".
        
            `UserData`

            Optional caller-supplied value, which CPSUI places in a <a href="..\compstui\ns-compstui-_cpsuicbparam.md">CPSUICBPARAM</a> structure's <b>UserData</b> member when calling the function pointed to by <b>pfnCallBack</b>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | compstui.h (include Compstui.h) |