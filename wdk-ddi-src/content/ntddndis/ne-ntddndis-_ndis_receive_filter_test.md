---
UID : NE:ntddndis._NDIS_RECEIVE_FILTER_TEST
title : _NDIS_RECEIVE_FILTER_TEST
author : windows-driver-content
description : The NDIS_RECEIVE_FILTER_TEST enumeration identifies the type of test that the receive filter performs.
old-location : netvista\ndis_receive_filter_test.htm
old-project : netvista
ms.assetid : 064d8335-3ebf-4bc2-901e-10ce46bf7732
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _NDIS_RECEIVE_FILTER_TEST, *PNDIS_RECEIVE_FILTER_TEST, NDIS_RECEIVE_FILTER_TEST
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : ntddndis.h
req.include-header : Ndis.h
req.target-type : Windows
req.target-min-winverclnt : Supported in NDIS 6.20 and later.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : NDIS_RECEIVE_FILTER_TEST
req.alt-loc : Ntddndis.h
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
req.typenames : "*PNDIS_RECEIVE_FILTER_TEST, NDIS_RECEIVE_FILTER_TEST"
---

# _NDIS_RECEIVE_FILTER_TEST Enumeration
The <b>NDIS_RECEIVE_FILTER_TEST</b> enumeration identifies the type of test that the receive filter
  performs.

## Syntax
````
typedef enum _NDIS_RECEIVE_FILTER_TEST { 
  NdisReceiveFilterTestUndefined,
  NdisReceiveFilterTestEqual,
  NdisReceiveFilterTestMaskEqual,
  NdisReceiveFilterTestNotEqual,
  NdisReceiveFilterTestMaximum
} NDIS_RECEIVE_FILTER_TEST, *PNDIS_RECEIVE_FILTER_TEST;
````

## Constants

<table>

<tr>
<td>NdisReceiveFilterTestEqual</td>
<td>The network adapter tests the selected header field to determine whether it is equal to a specific
     value.</td>
</tr>

<tr>
<td>NdisReceiveFilterTestMaskEqual</td>
<td>The network adapter supports masking (that is, a bitwise AND) of the selected header field to
     determine whether the result is equal to a specific value.</td>
</tr>

<tr>
<td>NdisReceiveFilterTestMaximum</td>
<td>The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.</td>
</tr>

<tr>
<td>NdisReceiveFilterTestNotEqual</td>
<td>The network adapter tests the selected header field to determine whether it is not equal to a specific
     value.</td>
</tr>

<tr>
<td>NdisReceiveFilterTestUndefined</td>
<td>The type of test is not specified.</td>
</tr>
</table>

## Remarks

The NDIS_RECEIVE_FILTER_TEST enumeration is used in the 
    <a href="..\ntddndis\ns-ntddndis-_ndis_receive_filter_field_parameters.md">
    NDIS_RECEIVE_FILTER_FIELD_PARAMETERS</a> structure.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ntddndis.h (include Ndis.h) |

## See Also

<dl>
<dt>
<a href="..\ntddndis\ns-ntddndis-_ndis_receive_filter_field_parameters.md">
   NDIS_RECEIVE_FILTER_FIELD_PARAMETERS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20NDIS_RECEIVE_FILTER_TEST enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>