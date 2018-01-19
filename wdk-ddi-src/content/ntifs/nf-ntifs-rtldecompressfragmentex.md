---
UID : NF:ntifs.RtlDecompressFragmentEx
title : RtlDecompressFragmentEx function
author : windows-driver-content
description : The RtlDecompressFragmentEx function is used to decompress part of a compressed buffer (that is, a buffer &#0034;fragment&#0034;), using multiple processors where possible.
old-location : ifsk\rtldecompressfragmentex.htm
old-project : ifsk
ms.assetid : A4FE108D-85CE-4F6A-A17A-E81684764FD3
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : RtlDecompressFragmentEx
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ntifs.h
req.include-header : Fltkernel.h, Ntifs.h
req.target-type : Universal
req.target-min-winverclnt : Available in starting in Windows 10.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : RtlDecompressFragmentEx
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


# RtlDecompressFragmentEx function
The <b>RtlDecompressFragmentEx</b> function is used to decompress part of a compressed buffer (that is, a buffer "fragment"), using multiple processors where possible.

## Syntax

````
NTSTATUS RtlDecompressFragmentEx(
  _In_  ULONG  CompressionFormat,
  _Out_ PUCHAR UncompressedFragment,
  _In_  ULONG  UncompressedFragmentSize,
  _In_  PUCHAR CompressedBuffer,
  _In_  ULONG  CompressedBufferSize,
  _In_  ULONG  FragmentOffset,
  _In_  ULONG  UncompressedChunkSize,
  _Out_ PULONG FinalUncompressedSize,
  _In_  PVOID  WorkSpace
);
````

## Parameters

`CompressionFormat`

Bitmask specifying the compression format of the compressed buffer. This parameter must be set to COMPRESSION_FORMAT_LZNT1. The meaning of this and other related compression format values are as follows:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
COMPRESSION_FORMAT_NONE

</td>
<td>
Not supported by this function.

</td>
</tr>
<tr>
<td>
COMPRESSION_FORMAT_DEFAULT

</td>
<td>
Not supported by this function.

</td>
</tr>
<tr>
<td>
COMPRESSION_FORMAT_LZNT1

</td>
<td>
Specifies that compression should be performed. This value is required.

</td>
</tr>
</table>

`UncompressedFragment`

Pointer to a caller-allocated buffer (allocated from paged or non-paged pool) receiving the decompressed data from <i>CompressedBuffer</i>. This parameter is required and cannot be <b>NULL</b>.

`UncompressedFragmentSize`

The size, in bytes, of the <i>UncompressedFragment</i> buffer.

`CompressedBuffer`

A pointer to the buffer containing the data to decompress. This parameter is required and cannot be <b>NULL</b>.

`CompressedBufferSize`

The size, in bytes, of the <i>CompressedBuffer</i> buffer.

`FragmentOffset`

The zero-based offset, in bytes, where the uncompressed fragment is being extract from. This offset value is the position within the original uncompressed buffer.

`UncompressedChunkSize`

The size, in bytes, of each chunk within the compression buffer.  Valid values are 512, 1024, 2048 and 4096.

`FinalUncompressedSize`

A pointer to a caller-allocated variable which receives the size, in bytes, of the decompressed data stored in <i>UncompressedFragment</i>. This parameter is required and cannot be <b>NULL</b>.

`WorkSpace`

A pointer to a caller-allocated work space buffer used by the <b>RtlDecompressFragmentEx</b> function during decompression. Use the <a href="..\ntifs\nf-ntifs-rtlgetcompressionworkspacesize.md">RtlGetCompressionWorkSpaceSize</a> function to determine the correct work space buffer size.


## Return Value

<a href="..\ntifs\nf-ntifs-rtldecompressfragment.md">RtlDecompressFragment</a>returns an appropriate error status, such as one of the following:
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The <i>CompressedBuffer</i> buffer was successfully decompressed into <i>UncompressedFragment</i>.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>An invalid compression format was specified via the <i>CompressionFormat</i> parameter. If <i>CompressionFormat</i> is either COMPRESSION_FORMAT_NONE or COMPRESSION_FORMAT_DEFAULT (but not both), this value is returned.
<dl>
<dt><b>STATUS_UNSUPPORTED_COMPRESSION</b></dt>
</dl>An invalid compression format was specified via the <i>CompressionFormat</i> parameter. If <i>CompressionFormat</i> is not one of the following, STATUS_UNSUPPORTED_COMPRESSION is returned:
<dl>
<dt><b>STATUS_BAD_COMPRESSION_BUFFER</b></dt>
</dl><i>UncompressedFragment</i> is not large enough to contain the uncompressed data.


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
<a href="..\ntifs\nf-ntifs-rtlcompressbuffer.md">RtlCompressBuffer</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtldecompressbuffer.md">RtlDecompressBuffer</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtldecompressbufferex.md">RtlDecompressBufferEx</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtldecompressbufferex2.md">RtlDecompressBufferEx2</a>
</dt>
<dt>
<a href="..\ntifs\nf-ntifs-rtldecompressfragment.md">RtlDecompressFragment</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20RtlDecompressFragmentEx routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>