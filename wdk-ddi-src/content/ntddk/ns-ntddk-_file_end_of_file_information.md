---
UID : NS:ntddk._FILE_END_OF_FILE_INFORMATION
title : _FILE_END_OF_FILE_INFORMATION
author : windows-driver-content
description : The FILE_END_OF_FILE_INFORMATION structure is used as an argument to the ZwSetInformationFile routine.
old-location : kernel\file_end_of_file_information.htm
old-project : kernel
ms.assetid : 9af172d9-2309-4731-82bf-55ec99c475a6
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _FILE_END_OF_FILE_INFORMATION, FILE_END_OF_FILE_INFORMATION, *PFILE_END_OF_FILE_INFORMATION
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ntddk.h
req.include-header : Ntddk.h, Ntifs.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : FILE_END_OF_FILE_INFORMATION
req.alt-loc : Ntddk.h
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
req.typenames : FILE_END_OF_FILE_INFORMATION, *PFILE_END_OF_FILE_INFORMATION
---

# _FILE_END_OF_FILE_INFORMATION structure
The <b>FILE_END_OF_FILE_INFORMATION</b> structure is used as an argument to the <a href="..\wdm\nf-wdm-zwsetinformationfile.md">ZwSetInformationFile</a> routine.

## Syntax
````
typedef struct _FILE_END_OF_FILE_INFORMATION {
  LARGE_INTEGER EndOfFile;
} FILE_END_OF_FILE_INFORMATION, *PFILE_END_OF_FILE_INFORMATION;
````

## Members

        
            `EndOfFile`

            The absolute new end of file position as a byte offset from the start of the file.

    ## Remarks
        <b>EndOfFile</b> specifies the byte offset to the end of the file. Because this value is zero-based, it actually refers to the first free byte in the file: that is, it is the offset to the byte immediately following the last valid byte in the file.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddk.h (include Ntddk.h, Ntifs.h) |

    ## See Also

        <dl>
<dt>
<a href="..\wdm\nf-wdm-zwqueryinformationfile.md">ZwQueryInformationFile</a>
</dt>
<dt>
<a href="..\wdm\nf-wdm-zwsetinformationfile.md">ZwSetInformationFile</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20FILE_END_OF_FILE_INFORMATION structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>