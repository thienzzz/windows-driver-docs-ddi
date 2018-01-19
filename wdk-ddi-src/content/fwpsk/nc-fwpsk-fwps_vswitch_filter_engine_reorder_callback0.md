---
UID : NC:fwpsk.FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0
title : FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0
author : windows-driver-content
description : The filter engine calls the vSwitchFilterEngineReorderNotifyRn (FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0) callout function to notify the callout driver about events that are associated the virtual switch filter engine reordering.Note  FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0 is a specific version of FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK. See WFP Version-Independent Names and Targeting Specific Versions of Windows for more information.
old-location : netvista\fwps_vswitch_filter_engine_reorder_callback0.htm
old-project : netvista
ms.assetid : 2526E8BD-316F-4B8D-9CC4-66F4E3B7D708
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : FwpmEngineOpen0
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : fwpsk.h
req.include-header : Fwpsk.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows 8.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : vSwitchFilterEngineReorderNotifyRn
req.alt-loc : fwpsk.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : <= DISPATCH_LEVEL
req.typenames : PINSTANCE_PARTIAL_INFORMATION, INSTANCE_PARTIAL_INFORMATION
---


# FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0 callback function
The filter engine calls the  
  
  <i>vSwitchFilterEngineReorderNotifyRn</i> (<i>FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0</i>) callout function to notify the callout driver about events that are
  associated the virtual switch  filter engine reordering.<div class="alert"><b>Note</b>  <i>FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0</i> is a specific version of <i>FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK</i>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div>
<div> </div>

## Syntax

```
FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0 FwpsVswitchFilterEngineReorderCallback0;

NTSTATUS FwpsVswitchFilterEngineReorderCallback0(
  void *notifyContext,
  void *completionContext,
  BOOLEAN isInRequiredPosition,
  const NDIS_ENUM_FILTERS *vSwitchExtensionLwfList
)
{...}
```

## Parameters

`*notifyContext`



`*completionContext`



`isInRequiredPosition`

A BOOLEAN value that is set to TRUE if the filter is in the required position in the filter stack or FALSE if it is not.

`*vSwitchExtensionLwfList`




## Return Value

A callout's 
  
  <i>FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0</i> function returns one of the following NTSTATUS codes.
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>The callout driver accepts the notification from the filter engine.
<dl>
<dt><b>Other status codes</b></dt>
</dl>An error occurred.

## Remarks

A callout driver registers a 
  
  <i>vSwitchFilterEngineReorderNotifyRn</i> function  by calling  
    
    the <a href="..\fwpsk\nf-fwpsk-fwpsvswitcheventssubscribe0.md">FwpsvSwitchEventsSubscribe0</a>
 function.

By default, the WFP virtual switch extension is positioned as the first filtering extension at virtual switch ingress. (Therefore, it is also the last extension at virtual switch egress). This is usually the best position, because the WFP extension can intercept packets before any other extensions can modify them at ingress. Also, the WFP extension can intercept packets after all packet modifications are done at egress.



However, because an administrator can reorder any virtual switch extensions of the same class, the WFP extension can be reordered out of the default position. After a reorder occurs, a WFP client’s filters could be bypassed and might need to be adjusted.

If the <i>vSwitchFilterEngineReorderNotifyRn</i> callback is registered, the callout driver is notified when a virtual switch reorder is occurring. The callout driver receives an <a href="..\ndis\ns-ndis-_ndis_enum_filters.md">NDIS_ENUM_FILTERS</a> structure with an ordered list of current virtual switch extensions in the <i>vSwitchExtensionLwfList</i> parameter.

If the virtual switch extensions are reordered, the WFP extension is  paused (see <a href="..\ndis\nc-ndis-filter_pause.md">FilterPause</a>) and restarted (see <a href="..\ndis\nc-ndis-filter_restart.md">FilterRestart</a>). From the WFP filter <i>FilterRestart</i> call, the WFP filter driver calls the <a href="..\ndis\nf-ndis-ndisenumeratefiltermodules.md">NdisEnumerateFilterModules</a> function to obtain an ordered list of virtual switch extension filters.  If the WFP extension is not in the default position, then the filter driver notifies the callout drivers.

A callout driver cannot return STATUS_PENDING from <i>vSwitchFilterEngineReorderNotifyRn</i>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | fwpsk.h (include Fwpsk.h) |
| **Library** |  |
| **IRQL** | <= DISPATCH_LEVEL |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\ndis\nc-ndis-filter_pause.md">FilterPause</a>
</dt>
<dt>
<a href="..\ndis\nc-ndis-filter_restart.md">FilterRestart</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpsvswitcheventssubscribe0.md">FwpsvSwitchEventsSubscribe0</a>
</dt>
<dt>
<a href="..\fwpsk\nf-fwpsk-fwpsvswitchnotifycomplete0.md">FwpsvSwitchNotifyComplete0</a>
</dt>
<dt>
<a href="..\ndis\ns-ndis-_ndis_enum_filters.md">NDIS_ENUM_FILTERS</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisenumeratefiltermodules.md">NdisEnumerateFilterModules</a>
</dt>
<dt>
<a href="..\ndis\nf-ndis-ndisfrestartcomplete.md">NdisFRestartComplete</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543875">Callout Driver Callout Functions</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20FWPS_VSWITCH_FILTER_ENGINE_REORDER_CALLBACK0 callback function%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>