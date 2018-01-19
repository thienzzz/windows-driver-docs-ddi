---
UID : NS:ntdddump._FILTER_INITIALIZATION_DATA
title : _FILTER_INITIALIZATION_DATA
author : windows-driver-content
description : The filter driver fills in a FILTER_INITIALIZATION_DATA structure and returns it to the crash dump driver.
old-location : storage\filter_initialization_data.htm
old-project : storage
ms.assetid : 71f9d0c2-ffc9-4fe1-ae95-f38a1d1e82df
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _FILTER_INITIALIZATION_DATA, *PFILTER_INITIALIZATION_DATA, FILTER_INITIALIZATION_DATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntdddump.h
req.include-header : Ntdddump.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows Vista and Windows Server 2008.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FILTER_INITIALIZATION_DATA
req.alt-loc : ntdddump.h
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
req.typenames : "*PFILTER_INITIALIZATION_DATA, FILTER_INITIALIZATION_DATA"
---

# _FILTER_INITIALIZATION_DATA structure
The filter driver fills in a <b>FILTER_INITIALIZATION_DATA</b> structure and returns it to the crash dump driver.

## Syntax
````
typedef struct _FILTER_INITIALIZATION_DATA {
  ULONG        MajorVersion;
  ULONG        MinorVersion;
  PDUMP_START  DumpStart;
  PDUMP_WRITE  DumpWrite;
  PDUMP_FINISH DumpFinish;
  PDUMP_UNLOAD DumpUnload;
  PVOID        DumpData;
  ULONG        MaxPagesPerWrite;
  ULONG        Flags;
  PDUMP_READ   DumpRead;
} FILTER_INITIALIZATION_DATA, *PFILTER_INITIALIZATION_DATA;
````

## Members

        
            `DumpData`

            The filter driver can pass a pointer to internal context data in this member. This pointer is passed back to the filter driver in a <a href="..\ntdddump\ns-ntdddump-_filter_extension.md">FILTER_EXTENSION</a> structure during each callback.
        
            `DumpFinish`

            A pointer to the dump finish routine.  This routine is called when the crash dump is finished.
        
            `DumpRead`

            A pointer to the read routine. This routine is called after every crash dump read request. This member is available starting in Windows 8.
        
            `DumpStart`

            A pointer to the dump initialization routine. This routine is called when the crash dump starts.
        
            `DumpUnload`

            A pointer to the dump unload routine. This routine is called before the driver is unloaded.
        
            `DumpWrite`

            A pointer to the write routine. This routine is called before every crash dump write request.
        
            `Flags`

            A set of flags for  dump filter initialization. This value is set to either 0 or the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
        
            `MajorVersion`

            Set to one of the following major version values:
        
            `MaxPagesPerWrite`

            The maximum number of pages for each dump read or write request.
        
            `MinorVersion`

            Set to <b>DUMP_FILTER_MINOR_VERSION</b>.

    ## Remarks
        For a dump filter driver to support read filtering, the following settings are required:

If any of these members are not set, the dump filter driver will be marked as not supporting dump reads by the crashdump stack.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntdddump.h (include Ntdddump.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ntdddump\nc-ntdddump-dump_finish.md">Dump_Finish</a>
</dt>
<dt>
<a href="..\ntdddump\nc-ntdddump-dump_read.md">Dump_Read</a>
</dt>
<dt>
<a href="..\ntdddump\nc-ntdddump-dump_start.md">Dump_Start</a>
</dt>
<dt>
<a href="..\ntdddump\nc-ntdddump-dump_write.md">Dump_Write</a>
</dt>
<dt>
<a href="..\ntdddump\nc-ntdddump-dump_unload.md">Dump_Unload</a>
</dt>
<dt>
<a href="..\ntdddump\ns-ntdddump-_filter_extension.md">FILTER_EXTENSION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20FILTER_INITIALIZATION_DATA structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>