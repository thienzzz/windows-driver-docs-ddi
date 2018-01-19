---
UID : NA:printoem
ms.assetid : 379c3ecf-1026-3228-91da-b4a57a86b3ce
ms.author : windowsdriverdev
ms.date : 01/18/18
ms.keywords : 
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : portal
---

# printoem.h header



printoem.h contains the following programming interfaces:





## Functions
| Title | Description |
| ---- |:---- |
| [OEMCUIPCALLBACK](nc-printoem-oemcuipcallback.md) | The OEMCUIPCALLBACK function type is used for defining callback functions that are specified by a user interface plug-in's IPrintOemUI::CommonUIProp method. The structure is defined in printoem.h. |
| [PFNGETINFO](nc-printoem-pfngetinfo.md) | The UNIFONTOBJ_GetInfo callback function is provided by the Unidrv driver so that rendering plug-ins can obtain font or glyph information. |
| [OEMAlphaBlend](nf-printoem-oemalphablend.md) | OEMAlphaBlend function |
| [OEMBitBlt](nf-printoem-oembitblt.md) | The OEMBitBlt function provides general bit-block transfer capabilities between device-managed surfaces, between GDI-managed standard-format bitmaps, or between a device-managed surface and a GDI-managed standard-format bitmap. |
| [OEMCommand](nf-printoem-oemcommand.md) | OEMCommand function |
| [OEMCommandCallback](nf-printoem-oemcommandcallback.md) | OEMCommandCallback function |
| [OEMCommonUIProp](nf-printoem-oemcommonuiprop.md) | OEMCommonUIProp function |
| [OEMCompression](nf-printoem-oemcompression.md) | OEMCompression function |
| [OEMCopyBits](nf-printoem-oemcopybits.md) | The OEMCopyBits function performs translations between device-managed raster surfaces and GDI standard-format bitmaps. |
| [OEMDeviceCapabilities](nf-printoem-oemdevicecapabilities.md) | OEMDeviceCapabilities function |
| [OEMDevicePropertySheets](nf-printoem-oemdevicepropertysheets.md) | OEMDevicePropertySheets function |
| [OEMDevMode](nf-printoem-oemdevmode.md) | OEMDevMode function |
| [OEMDevQueryPrintEx](nf-printoem-oemdevqueryprintex.md) | OEMDevQueryPrintEx function |
| [OEMDisableDriver](nf-printoem-oemdisabledriver.md) | OEMDisableDriver function |
| [OEMDisablePDEV](nf-printoem-oemdisablepdev.md) | OEMDisablePDEV function |
| [OEMDitherColor](nf-printoem-oemdithercolor.md) | The OEMDitherColor function requests the device to create a brush dithered against a device palette. |
| [OEMDocumentPropertySheets](nf-printoem-oemdocumentpropertysheets.md) | OEMDocumentPropertySheets function |
| [OEMDownloadCharGlyph](nf-printoem-oemdownloadcharglyph.md) | OEMDownloadCharGlyph function |
| [OEMDownloadFontHeader](nf-printoem-oemdownloadfontheader.md) | OEMDownloadFontHeader function |
| [OEMDriverDMS](nf-printoem-oemdriverdms.md) | OEMDriverDMS function |
| [OEMEnableDriver](nf-printoem-oemenabledriver.md) | OEMEnableDriver function |
| [OEMEnablePDEV](nf-printoem-oemenablepdev.md) | OEMEnablePDEV function |
| [OEMEndDoc](nf-printoem-oemenddoc.md) | The OEMEndDoc function is called by the GDI when it has finished sending a document to the driver for rendering. |
| [OEMEscape](nf-printoem-oemescape.md) | The OEMEscape function retrieves information from a device that is not available in a device-independent device driver interface; the particular query depends on the value of the iEsc parameter. |
| [OEMFillPath](nf-printoem-oemfillpath.md) | The OEMFillPath function handles the filling of closed paths. |
| [OEMFilterGraphics](nf-printoem-oemfiltergraphics.md) | OEMFilterGraphics function |
| [OEMFontInstallerDlgProc](nf-printoem-oemfontinstallerdlgproc.md) | OEMFontInstallerDlgProc function |
| [OEMFontManagement](nf-printoem-oemfontmanagement.md) | The OEMFontManagement function is an optional entry point provided for PostScript devices. |
| [OEMGetGlyphMode](nf-printoem-oemgetglyphmode.md) | The OEMGetGlyphMode function informs the GDI how to cache glyph information. |
| [OEMGetInfo](nf-printoem-oemgetinfo.md) | OEMGetInfo function |
| [OEMGradientFill](nf-printoem-oemgradientfill.md) | The OEMGradientFill function shades the specified primitives. |
| [OEMHalftonePattern](nf-printoem-oemhalftonepattern.md) | OEMHalftonePattern function |
| [OEMIcmCreateColorTransform](nf-printoem-oemicmcreatecolortransform.md) | The OEMIcmCreateColorTransform function creates an ICM color transform. |
| [OEMIcmDeleteColorTransform](nf-printoem-oemicmdeletecolortransform.md) | The OEMIcmDeleteColorTransform function deletes the specified color transform. |
| [OEMImageProcessing](nf-printoem-oemimageprocessing.md) | OEMImageProcessing function |
| [OEMLineTo](nf-printoem-oemlineto.md) | The OEMLineTo function draws a single, solid, integer-only cosmetic line. |
| [OEMNextBand](nf-printoem-oemnextband.md) | The OEMNextBand function is called by GDI when it has finished drawing a band for a physical page, so that the driver can send the band to the printer. |
| [OEMOutputCharStr](nf-printoem-oemoutputcharstr.md) | OEMOutputCharStr function |
| [OEMPaint](nf-printoem-oempaint.md) | The OEMPaint function is obsolete, and is no longer called by GDI in Windows 2000 and later. See DrvPaint. |
| [OEMPDriverEvent](nf-printoem-oempdriverevent.md) | OEMPDriverEvent function |
| [OEMPlgBlt](nf-printoem-oemplgblt.md) | The OEMPlgBlt function provides rotate bit-block transfer capabilities between combinations of device-managed and GDI-managed surfaces. |
| [OEMPrinterEvent](nf-printoem-oemprinterevent.md) | OEMPrinterEvent function |
| [OEMQueryAdvanceWidths](nf-printoem-oemqueryadvancewidths.md) | The OEMQueryAdvanceWidths function returns character advance widths for a specified set of glyphs. |
| [OEMQueryColorProfile](nf-printoem-oemquerycolorprofile.md) | OEMQueryColorProfile function |
| [OEMQueryDeviceSupport](nf-printoem-oemquerydevicesupport.md) | The OEMQueryDeviceSupport function returns requested device-specific information. |
| [OEMQueryFont](nf-printoem-oemqueryfont.md) | The OEMQueryFont function is used by GDI to get the IFIMETRICS structure for a given font. |
| [OEMQueryFontData](nf-printoem-oemqueryfontdata.md) | The OEMQueryFontData function retrieves information about a realized font. |
| [OEMQueryFontTree](nf-printoem-oemqueryfonttree.md) | The OEMQueryFontTree function provides GDI with a pointer to a structure that defines one of the following: |
| [OEMRealizeBrush](nf-printoem-oemrealizebrush.md) | The OEMRealizeBrush function requests that the driver realize a specified brush for a specified surface. |
| [OEMResetPDEV](nf-printoem-oemresetpdev.md) | OEMResetPDEV function |
| [OEMSendFontCmd](nf-printoem-oemsendfontcmd.md) | OEMSendFontCmd function |
| [OEMSendPage](nf-printoem-oemsendpage.md) | The OEMSendPage function is called by GDI when it has finished drawing a physical page, so that the driver can send the page to the printer. |
| [OEMStartBanding](nf-printoem-oemstartbanding.md) | The OEMStartBanding function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering. |
| [OEMStartDoc](nf-printoem-oemstartdoc.md) | The OEMStartDoc function is called by GDI when it is ready to start sending a document to the driver for rendering. |
| [OEMStartPage](nf-printoem-oemstartpage.md) | The OEMStartPage function is called by GDI when it is ready to start sending the contents of a physical page to the driver for rendering. |
| [OEMStretchBlt](nf-printoem-oemstretchblt.md) | The OEMStretchBlt function provides stretching bit-block transfer capabilities between any combination of device-managed and GDI-managed surfaces. |
| [OEMStretchBltROP](nf-printoem-oemstretchbltrop.md) | The OEMStretchBltROP function performs a stretching bit-block transfer using a raster operation (ROP). |
| [OEMStrokeAndFillPath](nf-printoem-oemstrokeandfillpath.md) | The OEMStrokeAndFillPath function concurrently strokes and fills a path. |
| [OEMStrokePath](nf-printoem-oemstrokepath.md) | The OEMStrokePath function strokes a path. |
| [OEMTextOut](nf-printoem-oemtextout.md) | The OEMTextOut function calls for the driver to render a set of glyphs at specified positions. |
| [OEMTextOutAsBitmap](nf-printoem-oemtextoutasbitmap.md) | OEMTextOutAsBitmap function |
| [OEMTransparentBlt](nf-printoem-oemtransparentblt.md) | The OEMTransparentBlt function provides bit-block transfer capabilities with transparency. |
| [OEMTTDownloadMethod](nf-printoem-oemttdownloadmethod.md) | OEMTTDownloadMethod function |
| [OEMTTYGetInfo](nf-printoem-oemttygetinfo.md) | OEMTTYGetInfo function |
| [OEMUpdateExternalFonts](nf-printoem-oemupdateexternalfonts.md) | OEMUpdateExternalFonts function |
| [OEMUpgradePrinter](nf-printoem-oemupgradeprinter.md) | OEMUpgradePrinter function |
| [OEMUpgradeRegistry](nf-printoem-oemupgraderegistry.md) | OEMUpgradeRegistry function |



## Structures
| Title | Description |
| ---- |:---- |
| [_CUSTOMSIZEPARAM](ns-printoem-_customsizeparam.md) | The CUSTOMSIZEPARAM structure holds information pertaining to a single custom page size parameter for a printer. |
| [_DEVOBJ](ns-printoem-_devobj.md) | The DEVOBJ structure is used as an input argument to several of a rendering plug-in's COM interface methods. |
| [_DRVPROCS](ns-printoem-_drvprocs.md) | The DRVPROCS structure is obsolete and is not used with the COM interfaces for Microsoft printer drivers. |
| [_FINVOCATION](ns-printoem-_finvocation.md) | The FINVOCATION structure is used as input to the IPrintOemUni::SendFontCmd method. The structure is defined in printoem.h. |
| [_GETINFO_FONTOBJ](ns-printoem-_getinfo_fontobj.md) | The GETINFO_FONTOBJ structure is used as input to the UNIFONTOBJ_GetInfo callback function. |
| [_GETINFO_GLYPHBITMAP](ns-printoem-_getinfo_glyphbitmap.md) | The GETINFO_GLYPHBITMAP structure is used as input to the UNIFONTOBJ_GetInfo callback function. |
| [_GETINFO_GLYPHSTRING](ns-printoem-_getinfo_glyphstring.md) | The GETINFO_GLYPHSTRING structure is used as input to the UNIFONTOBJ_GetInfo callback function. |
| [_GETINFO_GLYPHWIDTH](ns-printoem-_getinfo_glyphwidth.md) | The GETINFO_GLYPHWIDTH structure is used as input to the UNIFONTOBJ_GetInfo callback function. |
| [_GETINFO_MEMORY](ns-printoem-_getinfo_memory.md) | The GETINFO_MEMORY structure is used as input to the UNIFONTOBJ_GetInfo callback function. |
| [_GETINFO_STDVAR](ns-printoem-_getinfo_stdvar.md) | The GETINFO_STDVAR structure is used as input to the UNIFONTOBJ_GetInfo callback function. |
| [_OEM_DMEXTRAHEADER](ns-printoem-_oem_dmextraheader.md) | The OEM_DMEXTRAHEADER structure must be used to define the first members of a set of private DEVMODEW structure members. |
| [_OEMCUIPPARAM](ns-printoem-_oemcuipparam.md) | The OEMCUIPPARAM structure is used as an input parameter to a user interface plug-in's IPrintOemUI::CommonUIProp method. |
| [_OEMDMPARAM](ns-printoem-_oemdmparam.md) | The OEMDMPARAM structure is used as an input parameter to the IPrintOemUI::DevMode, IPrintOemUni::DevMode, and IPrintOemPS::DevMode methods. |
| [_OEMUIOBJ](ns-printoem-_oemuiobj.md) | The OEMUIOBJ structure is used as an input argument to several of the methods exported by user interface plug-ins. |
| [_OEMUIPROCS](ns-printoem-_oemuiprocs.md) | The OEMUIPROCS structure is obsolete.The OEMUIPROCS structure contains the address of the DrvGetDriverSetting and DrvUpdateUISetting functions that are exported by Microsoft printer drivers. |
| [_OEMUIPSPARAM](ns-printoem-_oemuipsparam.md) | The OEMUIPSPARAM structure is passed to a user interface plug-in's IPrintOemUI::DevicePropertySheets and IPrintOemUI::DocumentPropertySheets methods. |
| [_PDEV_ADJUST_GRAPHICS_RESOLUTION](ns-printoem-_pdev_adjust_graphics_resolution.md) | The PDEV_ADJUST_GRAPHICS_RESOLUTION structure specifies a graphics resolution value. |
| [_PDEV_ADJUST_IMAGEABLE_ORIGIN_AREA](ns-printoem-_pdev_adjust_imageable_origin_area.md) | The PDEV_ADJUST_IMAGEABLE_ORIGIN_AREA structure specifies the imageable origin area. |
| [_PDEV_ADJUST_PAPER_MARGIN](ns-printoem-_pdev_adjust_paper_margin.md) | The PDEV_ADJUST_PAPER_MARGIN structure specifies the imageable printing area. |
| [_PDEV_ADJUST_PHYSICAL_PAPER_SIZE](ns-printoem-_pdev_adjust_physical_paper_size.md) | The PDEV_ADJUST_PAPER_PHYSICAL_SIZE structure specifies a paper size value. |
| [_PDEV_HOSTFONT_ENABLED](ns-printoem-_pdev_hostfont_enabled.md) | The PDEV_HOSTFONT_ENABLED structure indicates whether the Hostfont feature is enabled. |
| [_PDEV_USE_TRUE_COLOR](ns-printoem-_pdev_use_true_color.md) | The PDEV_USE_TRUE_COLOR structure indicates whether the output color space should be color or grayscale. |
| [_PSCRIPT5_PRIVATE_DEVMODE](ns-printoem-_pscript5_private_devmode.md) | The PSCRIPT5_PRIVATE_DEVMODE structure enables Pscript5 plug-ins to determine the size of the private portion of Pscript5's DEVMODEW structure. |
| [_PUBLISHERINFO](ns-printoem-_publisherinfo.md) | The PUBLISHERINFO structure is used as an input parameter to the IPrintOemPS::GetInfo method. |
| [_SIMULATE_CAPS_1](ns-printoem-_simulate_caps_1.md) | The SIMULATE_CAPS_1 structure contains information about the types of simulations a spooler supports. |
| [_UNIDRV_PRIVATE_DEVMODE](ns-printoem-_unidrv_private_devmode.md) | The UNIDRV_PRIVATE_DEVMODE structure enables Unidrv plug-ins to determine the size of the private portion of Unidrv's DEVMODEW structure. |
| [_UNIFONTOBJ](ns-printoem-_unifontobj.md) | The UNIFONTOBJ structure is used as an input parameter to font functions in rendering plug-ins. |
| [_USERDATA](ns-printoem-_userdata.md) | The USERDATA structure is used by Unidrv and Pscript to specify additional information about printer features. A USERDATA structure pointer is supplied as the UserData member for each OPTITEM structure. |
| [IPPARAMS](ns-printoem-ipparams.md) | The IPPARAMS structure is used as an input parameter to a rendering plug-in's IPrintOemUni::ImageProcessing method. |
| [OEMMEMORYUSAGE](ns-printoem-oemmemoryusage.md) | The OEMMEMORYUSAGE structure is used as an input parameter to a rendering plug-in's IPrintOemUni::MemoryUsage method. |


## Enumerations
| Title | Description |
| ---- |:---- |
| [_EATTRIBUTE_DATATYPE](ne-printoem-_eattribute_datatype.md) | The EATTRIBUTE_DATATYPE enumerates the possible data types for a global attribute, feature attribute or option attribute. |
| [_STDVARIABLEINDEX](ne-printoem-_stdvariableindex.md) | . |