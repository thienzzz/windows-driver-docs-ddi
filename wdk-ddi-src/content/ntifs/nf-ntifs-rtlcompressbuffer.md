---
UID : NF:ntifs.RtlCompressBuffer
title : RtlCompressBuffer function
author : windows-driver-content
description : The RtlCompressBuffer function compresses a buffer and can be used by a file system driver to facilitate the implementation of file compression.
old-location : ifsk\rtlcompressbuffer.htm
old-project : ifsk
ms.assetid : 49fb1062-9709-4691-9655-8cbf3c5055fb
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RtlCompressBuffer
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Fltkernel.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available starting in Windows XP.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlCompressBuffer
req.alt-loc : NtosKrnl.exe
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : NtosKrnl.lib
req.dll : NtosKrnl.exe
req.irql : <= APC_LEVEL
req.typenames : TOKEN_TYPE
---


# RtlCompressBuffer function
The <b>RtlCompressBuffer</b> function compresses a buffer and can be used by a file system driver to facilitate the implementation of file compression.

## Syntax

````
NTSTATUS RtlCompressBuffer(
  _In_  USHORT CompressionFormatAndEngine,
  _In_  PUCHAR UncompressedBuffer,
  _In_  ULONG  UncompressedBufferSize,
  _Out_ PUCHAR CompressedBuffer,
  _In_  ULONG  CompressedBufferSize,
  _In_  ULONG  UncompressedChunkSize,
  _Out_ PULONG FinalCompressedSize,
  _In_  PVOID  WorkSpace
);
````

## Parameters

`CompressionFormatAndEngine`

A bitmask that specifies the compression format and engine type. This parameter must be set to  a  valid bitwise OR combination of one format type and one engine type. For example, COMPRESSION_FORMAT_LZNT1 | COMPRESSION_ENGINE_STANDARD.

The meanings of these, and other related values, are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>

`UncompressedBuffer`

A pointer to a caller-allocated buffer (allocated from paged or non-paged pool) that contains the data to be compressed. This parameter is required and cannot be <b>NULL</b>.

`UncompressedBufferSize`

The size, in bytes, of the <i>UncompressedBuffer</i> buffer.

`CompressedBuffer`

A pointer to a caller-allocated buffer (allocated from paged or non-paged pool) that receives the compressed data. This parameter is required and cannot be <b>NULL</b>.

`CompressedBufferSize`

The size, in bytes, of the <i>CompressedBuffer</i> buffer.

`UncompressedChunkSize`

The chunk size to use when compressing the <i>UncompressedBuffer</i> buffer. This parameter must be one of the following values:  512, 1024, 2048, or 4096. The operating system uses 4096, and the recommended value for this parameter is also 4096.

`FinalCompressedSize`

A pointer to a caller-allocated variable that receives the size, in bytes, of the compressed data stored in <i>CompressedBuffer</i>. This parameter is required and cannot be <b>NULL</b>.

`WorkSpace`

A pointer to a caller-allocated work space buffer used by the <b>RtlCompressBuffer</b> function during compression. Use the <a href="..\ntifs\nf-ntifs-rtlgetcompressionworkspacesize.md">RtlGetCompressionWorkSpaceSize</a> function to determine the correct work space buffer size.


## Return Value

<b>RtlCompressBuffer</b> returns an appropriate error status value, such as one of the following.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The <i>UncompressedBuffer</i> buffer was successfully compressed.
<dl>
<dt><b>STATUS_BUFFER_ALL_ZEROS</b></dt>
</dl>The <i>UncompressedBuffer</i> buffer was successfully compressed, but this buffer contains only zeros.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl><dl>
<dt><b>STATUS_UNSUPPORTED_COMPRESSION</b></dt>
</dl>COMPRESSION_FORMAT_LZNT1

 COMPRESSION_FORMAT_XPRESS

 COMPRESSION_FORMAT_XPRESS_HUFF

COMPRESSION_FORMAT_NONE (in this case, STATUS_INVALID_PARAMETER is returned)

COMPRESSION_FORMAT_DEFAULT (in this case, STATUS_INVALID_PARAMETER is returned)
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>An invalid compression engine was specified through the <i>CompressionFormatAndEngine</i> parameter. If <i>CompressionFormatAndEngine</i> is not COMPRESSION_ENGINE_STANDARD or COMPRESSION_ENGINE_MAXIMUM (but not both), this value is returned.
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>The compressed buffer is too small to hold the compressed data. That is, <i>FinalCompressedSize</i> is greater than <i>CompressedBufferSize</i>.

## Remarks

The <b>RtlCompressBuffer</b> function takes as input an uncompressed buffer and produces its compressed equivalent provided that the compressed data fits within the specified destination buffer.

To determine the correct buffer size for the <i>WorkSpace</i> parameter, use the <a href="..\ntifs\nf-ntifs-rtlgetcompressionworkspacesize.md">RtlGetCompressionWorkSpaceSize</a> function.

To decompress a compressed buffer, use the <a href="..\ntifs\nf-ntifs-rtldecompressbuffer.md">RtlDecompressBuffer</a> function.

To extract an uncompressed fragment from a compressed buffer, use the <a href="..\ntifs\nf-ntifs-rtldecompressfragment.md">RtlDecompressFragment</a> function.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntifs.h (include Fltkernel.h, Ntifs.h) |
| **Library** |  |
| **IRQL** | <= APC_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ntifs\ns-ntifs-_file_compression_information.md">FILE_COMPRESSION_INFORMATION</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtldecompressbuffer.md">RtlDecompressBuffer</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtldecompressfragment.md">RtlDecompressFragment</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtlgetcompressionworkspacesize.md">RtlGetCompressionWorkSpaceSize</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RtlCompressBuffer function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>