---
UID : NS:d3dkmddi._DXGK_SEGMENTFLAGS
title : _DXGK_SEGMENTFLAGS
author : windows-driver-content
description : The DXGK_SEGMENTFLAGS structure identifies properties for a segment that the driver provides through a call to its DxgkDdiQueryAdapterInfo function.
old-location : display\dxgk_segmentflags.htm
old-project : display
ms.assetid : 959dfdb2-cadf-427d-958a-33ce2a1610ae
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _DXGK_SEGMENTFLAGS, DXGK_SEGMENTFLAGS
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3dkmddi.h
req.include-header : D3dkmddi.h
req.target-type : Windows
req.target-min-winverclnt : Available starting with Windows Vista.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DXGK_SEGMENTFLAGS
req.alt-loc : d3dkmddi.h
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
req.typenames : DXGK_SEGMENTFLAGS
---

# _DXGK_SEGMENTFLAGS structure
The DXGK_SEGMENTFLAGS structure identifies properties for a segment that the driver provides through a call to its <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_queryadapterinfo.md">DxgkDdiQueryAdapterInfo</a> function.

## Syntax
````
typedef struct _DXGK_SEGMENTFLAGS {
  union {
    struct {
      UINT Aperture  :1;
      UINT Agp  :1;
      UINT CpuVisible  :1;
      UINT UseBanking  :1;
      UINT CacheCoherent  :1;
      UINT PitchAlignment  :1;
      UINT PopulatedFromSystemMemory  :1;
      UINT PreservedDuringStandby  :1;
      UINT PreservedDuringHibernate  :1;
      UINT PartiallyPreservedDuringHibernate  :1;
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WIN8)
      UINT DirectFlip  :1;
#if (DXGKDDI_INTERFACE_VERSION >= DXGKDDI_INTERFACE_VERSION_WDDM2_0)
      UINT Use64KBPages  :1;
      UINT ReservedSysMem  :1;
      UINT SupportsCpuHostAperture  :1;
      UINT SupportsCachedCpuHostAperture  :1;
      UINT ApplicationTarget  :1;
      UINT Reserved  :16;
#else 
      UINT Reserved  :21;
#endif 
#else 
      UINT Reserved  :22;
#endif 
    };
    UINT Value;
  };
} DXGK_SEGMENTFLAGS;
````

## Members


    ## Remarks
        The driver can specify properties of the segment by setting bits in the 32-bit <b>Value</b> member or by setting individual members of the structure in the union that DXGK_SEGMENTFLAGS contains.

Note that for an AGP-type aperture segment, the driver must exclusively set the <b>Agp</b> member of the structure in the union that DXGK_SEGMENTFLAGS contains. Although the AGP-type aperture segment is an aperture and visible to the CPU, if any other members are set, the adapter fails to initialize.

In the special case where the allocation uses an aperture segment on a shared primary allocation (<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_getstandardallocationdriverdata.md">DXGKARG_GETSTANDARDALLOCATIONDRIVERDATA</a>.<b>StandardAllocationType</b> is <b>D3DKMDT_STANDARDALLOCATION_SHAREDPRIMARYSURFACE</b>), and <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_allocationinfoflags.md">DXGK_ALLOCATIONINFOFLAGS</a>.<b>UseAlternateVA</b> is not set,  the driver should use a section-backed primary allocation (<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_vidmmcaps.md">DXGK_VIDMMCAPS</a>.<b>SectionBackedPrimary</b> is set) when the driver's <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_queryadapterinfo.md">DxgkDdiQueryAdapterInfo</a> function is called. By using a section-backed primary you can avoid the limitations of <b>CpuVisible</b> for the aperture segment.

You can avoid the limitations of <b>CpuVisible</b> for an aperture segment by using a shared, section-backed primary allocation. In this case, use an aperture segment on a shared primary allocation (<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_getstandardallocationdriverdata.md">DXGKARG_GETSTANDARDALLOCATIONDRIVERDATA</a>.<b>StandardAllocationType</b> is <b>D3DKMDT_STANDARDALLOCATION_SHAREDPRIMARYSURFACE</b>), do not set <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_allocationinfoflags.md">DXGK_ALLOCATIONINFOFLAGS</a>.<b>UseAlternateVA</b>,  and use a section-backed primary allocation (set <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_vidmmcaps.md">DXGK_VIDMMCAPS</a>.<b>SectionBackedPrimary</b>) when the driver's <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_queryadapterinfo.md">DxgkDdiQueryAdapterInfo</a> function is called. 

The combination of values for the <b>PreservedDuringStandby</b>, <b>PreservedDuringHibernate</b>, and  <b>PartiallyPreservedDuringHibernate</b> members determines whether a segment is purged of its content when the system enters a low-power (standby) system state, as follows.

The operating system does not recognize combinations in this table that are marked "invalid."

If the <a href="https://msdn.microsoft.com/library/windows/hardware/mt608297">hybrid sleep</a> mode is enabled, the system acts as if it is hibernating: it purges segments that are not preserved during hibernate, even if it is going into a low-power state.


The following are common combinations of member values.



The following are common combinations of member values.

The segment is never purged during a power transition. This combination of member values should be set on memory segments that are populated from driver-allocated system memory—not BIOS-reserved memory, which is not automatically preserved in the hibernate state. These two members should also both be set for aperture segments in which page table content should be preserved during power transitions.

The segment is preserved during a sleep state but purged during a hibernate state. This combination of member values should be used for memory segments that are populated from BIOS-reserved memory, or for memory and aperture segments that are exposed by a discrete GPU that keeps its VRAM refreshed during a sleep state.

The segment is preserved during a sleep state. In addition, during a hibernate state, only those allocations beyond the memory address specified by the <b>SystemMemoryEndAddress</b> member of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_segmentdescriptor3.md">DXGK_SEGMENTDESCRIPTOR3</a> structure are evicted.

This combination of member values should be set on memory segments that are populated partially from driver-allocated memory and partially from BIOS-reserved memory. <b>PartiallyPreservedDuringHibernate</b> and <b>PreservedDuringHibernate</b> cannot both be set on the same segment, and they cannot be set on aperture segments.

The segment is purged during all power transitions.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3dkmddi.h (include D3dkmddi.h) |

    ## See Also

        <dl>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_allocationinfo.md">DXGK_ALLOCATIONINFO</a>
</dt>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_querysegmentin.md">DXGK_QUERYSEGMENTIN</a>
</dt>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_segmentdescriptor.md">DXGK_SEGMENTDESCRIPTOR</a>
</dt>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_segmentdescriptor3.md">DXGK_SEGMENTDESCRIPTOR3</a>
</dt>
<dt>
<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_queryadapterinfo.md">DXGKARG_QUERYADAPTERINFO</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_buildpagingbuffer.md">DxgkDdiBuildPagingBuffer</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_queryadapterinfo.md">DxgkDdiQueryAdapterInfo</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGK_SEGMENTFLAGS structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>