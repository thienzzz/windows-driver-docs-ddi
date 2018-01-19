---
UID : NF:ks.KsFilterAddTopologyConnections
title : KsFilterAddTopologyConnections function
author : windows-driver-content
description : The KsFilterAddTopologyConnections function adds new topology connections to a filter.
old-location : stream\ksfilteraddtopologyconnections.htm
old-project : stream
ms.assetid : 32a61103-5f2f-4b73-a299-bf6a14c3bec9
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : KsFilterAddTopologyConnections
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : function
req.header : ks.h
req.include-header : Ks.h
req.target-type : Universal
req.target-min-winverclnt : Available in Microsoft Windows XP and later operating systems and DirectX 8.0 and later DirectX versions.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KsFilterAddTopologyConnections
req.alt-loc : Ks.lib,Ks.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Ks.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : 
---


# KsFilterAddTopologyConnections function
The<b> KsFilterAddTopologyConnections</b> function adds new topology connections to a filter.

## Syntax

````
NTSTATUS KsFilterAddTopologyConnections(
  _In_       PKSFILTER             Filter,
  _In_       ULONG                 NewConnectionsCount,
  _In_ const KSTOPOLOGY_CONNECTION *NewTopologyConnections
);
````

## Parameters

`Filter`

<i>A pointer</i> to the <a href="..\ks\ns-ks-_ksfilter.md">KSFILTER</a> to which to add the new connections.

`NewConnectionsCount`

The number of connections in <i>NewTopologyConnections</i>.

`NewTopologyConnections`

A pointer to an array of <a href="..\ks\ns-ks-kstopology_connection.md">KSTOPOLOGY_CONNECTION</a> structures containing the new topology connections.


## Return Value

<b>KsFilterAddTopologyConnections </b>returns STATUS_SUCCESS or an error code indicating failure of the attempt to add topology connections.

## Remarks

Note that the filter control mutex must be held before calling this function.

For more information about mutexes, see <a href="https://msdn.microsoft.com/011edaaa-7449-41c3-8cfb-0d319901af8b">Mutexes in AVStream</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ks.h (include Ks.h) |
| **Library** |  |
| **IRQL** | PASSIVE_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ks\ns-ks-_ksfilter.md">KSFILTER</a>
</dt>
<dt>
<a href="..\ks\ns-ks-kstopology_connection.md">KSTOPOLOGY_CONNECTION</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KsFilterAddTopologyConnections function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>