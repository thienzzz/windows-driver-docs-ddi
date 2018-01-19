---
UID : NC:d3d10umddi.PFND3DWDDM1_3DDI_UPDATETILEMAPPINGS
title : PFND3DWDDM1_3DDI_UPDATETILEMAPPINGS
author : windows-driver-content
description : Updates mappings of tile locations in tiled resources to memory locations in a tile pool.
old-location : display\updatetilemappings.htm
old-project : display
ms.assetid : 1C8FC920-145F-4AE9-B049-F6BDAE29D1F1
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : _SETRESULT_INFO, *PSETRESULT_INFO, SETRESULT_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Desktop
req.target-min-winverclnt : Windows 8.1,WDDM 1.3
req.target-min-winversvr : Windows Server 2012 R2
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : UpdateTileMappings
req.alt-loc : D3d10umddi.h
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
req.typenames : "*PSETRESULT_INFO, SETRESULT_INFO"
---


# PFND3DWDDM1_3DDI_UPDATETILEMAPPINGS callback function
Updates mappings of tile locations in tiled resources to memory locations in a tile pool.

## Syntax

```
PFND3DWDDM1_3DDI_UPDATETILEMAPPINGS Pfnd3dwddm13DdiUpdatetilemappings;

void Pfnd3dwddm13DdiUpdatetilemappings(
  D3D10DDI_HDEVICE hDevice,
  D3D10DDI_HRESOURCE hTiledResource,
  UINT NumTiledResourceRegions,
  const D3DWDDM1_3DDI_TILED_RESOURCE_COORDINATE *pTiledResourceRegionStartCoords,
  const D3DWDDM1_3DDI_TILE_REGION_SIZE *pTiledResourceRegionSizes,
  D3D10DDI_HRESOURCE hTilePool,
  UINT NumRanges,
  const UINT *pRangeFlags,
  const UINT *pTilePoolStartOffsets,
  const UINT *pRangeTileCounts,
  UINT Flags
)
{...}
```

## Parameters

`hDevice`

A handle to the display device (graphics context).

`hTiledResource`

A handle to the tiled resource.

`NumTiledResourceRegions`

The number of tiled resource regions.

`*pTiledResourceRegionStartCoords`



`*pTiledResourceRegionSizes`



`hTilePool`

A handle to the tile pool.

`NumRanges`

The number of tile-pool ranges.

`*pRangeFlags`



`*pTilePoolStartOffsets`



`*pRangeTileCounts`



`Flags`

A combination of <a href="..\d3d10umddi\ne-d3d10umddi-d3dwddm1_3ddi_tile_mapping_flag.md">D3DWDDM1_3DDI_TILE_MAPPING_FLAG</a> values that are combined by using a bitwise <b>OR</b> operation.


## Return Value

None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. The driver can set <b>E_INVALIDARG</b> if a required input parameter does not exist or is <b>NULL</b>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\d3d10umddi\ne-d3d10umddi-d3dwddm1_3ddi_tile_mapping_flag.md">D3DWDDM1_3DDI_TILE_MAPPING_FLAG</a>
</dt>
<dt>
<a href="..\d3d10umddi\ne-d3d10umddi-d3dwddm1_3ddi_tile_range_flag.md">D3DWDDM1_3DDI_TILE_RANGE_FLAG</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3dwddm1_3ddi_tile_region_size.md">D3DWDDM1_3DDI_TILE_REGION_SIZE</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3dwddm1_3ddi_tiled_resource_coordinate.md">D3DWDDM1_3DDI_TILED_RESOURCE_COORDINATE</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DWDDM1_3DDI_UPDATETILEMAPPINGS callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>