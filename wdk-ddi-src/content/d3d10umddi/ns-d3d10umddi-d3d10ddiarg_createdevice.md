---
UID : NS:d3d10umddi.D3D10DDIARG_CREATEDEVICE
title : D3D10DDIARG_CREATEDEVICE
author : windows-driver-content
description : The D3D10DDIARG_CREATEDEVICE structure describes the display device to create.
old-location : display\d3d10ddiarg_createdevice.htm
old-project : display
ms.assetid : 64154d8a-1775-455b-bf31-9c3a0f1398ad
ms.author : windowsdriverdev
ms.date : 12/29/2017
ms.keywords : D3D10DDIARG_CREATEDEVICE, D3D10DDIARG_CREATEDEVICE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : d3d10umddi.h
req.include-header : D3d10umddi.h
req.target-type : Windows
req.target-min-winverclnt : Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : D3D10DDIARG_CREATEDEVICE
req.alt-loc : d3d10umddi.h
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
req.typenames : D3D10DDIARG_CREATEDEVICE
---

# D3D10DDIARG_CREATEDEVICE structure
The <b>D3D10DDIARG_CREATEDEVICE</b> structure describes the display device to create.

## Syntax
````
typedef struct D3D10DDIARG_CREATEDEVICE {
  D3D10DDI_HRTDEVICE            hRTDevice;
  UINT                          Interface;
  UINT                          Version;
  const D3DDDI_DEVICECALLBACKS  *pKTCallbacks;
  union {
    D3D10DDI_DEVICEFUNCS      *pDeviceFuncs;
#if D3D10DDI_MINOR_HEADER_VERSION >= 1 || D3D11DDI_MINOR_HEADER_VERSION >= 1
    D3D10_1DDI_DEVICEFUNCS    *p10_1DeviceFuncs;
#endif 
#if D3D11DDI_MINOR_HEADER_VERSION >= 1
    D3D11DDI_DEVICEFUNCS      *p11DeviceFuncs;
#endif 
#if D3D11DDI_MINOR_HEADER_VERSION >= 3
    D3D11_1DDI_DEVICEFUNCS    *p11_1DeviceFuncs;
#endif 
#if D3D11DDI_MINOR_HEADER_VERSION >= 4
    D3DWDDM1_3DDI_DEVICEFUNCS *pWDDM1_3DeviceFuncs;
#endif 
  };
  D3D10DDI_HDEVICE              hDrvDevice;
  DXGI_DDI_BASE_ARGS            DXGIBaseDDI;
  D3D10DDI_HRTCORELAYER         hRTCoreLayer;
  union {
    const D3D10DDI_CORELAYER_DEVICECALLBACKS *pUMCallbacks;
#if D3D11DDI_MINOR_HEADER_VERSION >= 1
    const D3D11DDI_CORELAYER_DEVICECALLBACKS *p11UMCallbacks;
#endif 
  };
  UINT                          Flags;
#if D3D11DDI_MINOR_HEADER_VERSION >= 3
  PFND3D10DDI_RETRIEVESUBOBJECT *ppfnRetrieveSubObject;
#endif 
} D3D10DDIARG_CREATEDEVICE;
````

## Members

        
            `DXGIBaseDDI`

            [in/out] A <a href="..\dxgiddi\ns-dxgiddi-dxgi_ddi_base_args.md">DXGI_DDI_BASE_ARGS</a> structure that provides access to the DXGI. The DXGI DDI handles low-level tasks like presenting rendered frames to an output, controlling gamma, and managing a full-screen transition.
        
            `Flags`

            [in] A valid bitwise OR of flag values that identify how to create the display device. The Direct3D runtime supports the following flags:
        
            `hDrvDevice`

            [in/out] A handle to the display device (graphics context) that the Direct3D runtime uses in subsequent driver calls to identify the display device.
        
            `hRTCoreLayer`

            [in] A handle that the driver should use when it calls back into the Direct3D runtime to access core Direct3D 10 functionality (that is, when the driver calls functions that the <b>pUMCallbacks</b> member specifies).
        
            `hRTDevice`

            [in] A handle to the display device (graphics context) that specifies the handle that the driver should use when it calls back into the Direct3D runtime (that is, when the driver calls functions that the <b>pKTCallbacks</b> member specifies).
        
            `Interface`

            [in] The Direct3D interface version. The high 16 bits store the major release number (such as 10, 11, and so on); the low 16 bits store the minor release number (such as 0, 1, 2, and so on). The minor release number will be increased when a change to the interface is released.
        
            `pKTCallbacks`

            [in] A pointer to a <a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicecallbacks.md">D3DDDI_DEVICECALLBACKS</a> structure that contains a table of Direct3D runtime callback functions that the driver can use to access kernel services.
        
            `ppfnRetrieveSubObject`

            [in/out] A pointer to a <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_retrievesubobject.md">RetrieveSubObject(D3D11_1)</a> function that retrieves subparts of a Direct3D driver device object.

Supported starting with Windows 8.
        
            `Version`

            [in] A number that the driver can use to identify when the Direct3D runtime was built. The high 16 bits represent the build number; the low 16 bits represent the revision number. 

The driver is required only to monitor the high 16 bits. The driver should ensure that the runtime build version that is passed in is greater than or equal to the current build version of the driver. The driver should return a failure from its <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a> function if the passed in build version is incompatible.

    ## Remarks
        The driver examines values in the <b>Interface</b> and <b>Version</b> members to determine whether to fill the <a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>, <a href="..\d3d10umddi\ns-d3d10umddi-d3d10_1ddi_devicefuncs.md">D3D10_1DDI_DEVICEFUNCS</a>, <a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>, <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_devicefuncs.md">D3D11_1DDI_DEVICEFUNCS</a>, or <a href="..\d3d10umddi\ns-d3d10umddi-d3dwddm1_3ddi_devicefuncs.md">D3DWDDM1_3DDI_DEVICEFUNCS</a> structure that the <b>pDeviceFuncs</b>, <b>p10_1DeviceFuncs</b>, <b>p11DeviceFuncs</b>, <b>p11_1DeviceFuncs</b>, or  <b>pWDDM1_3DeviceFuncs</b> member points to with the driver's functions. The following constants from D3d10umddi.h are examples of the constants that the driver might find in <b>Interface</b> and <b>Version</b>:

Other possible combinations of constants for different versions of the operating system, Direct3D, and Windows Display Driver Model (WDDM) are listed in the D3d10umddi.h header.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | d3d10umddi.h (include D3d10umddi.h) |

    ## See Also

        <dl>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d10_1ddi_devicefuncs.md">D3D10_1DDI_DEVICEFUNCS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_corelayer_devicecallbacks.md">D3D10DDI_CORELAYER_DEVICECALLBACKS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_corelayer_devicecallbacks.md">D3D11DDI_CORELAYER_DEVICECALLBACKS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_devicefuncs.md">D3D11_1DDI_DEVICEFUNCS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ne-d3d10umddi-d3d11ddi_3dpipelinelevel.md">D3D11DDI_3DPIPELINELEVEL</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_3dpipelinesupport_caps.md">D3D11DDI_3DPIPELINESUPPORT_CAPS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>
</dt>
<dt>
<a href="..\d3d10umddi\ns-d3d10umddi-d3dwddm1_3ddi_devicefuncs.md">D3DWDDM1_3DDI_DEVICEFUNCS</a>
</dt>
<dt>
<a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_allocationlist.md">D3DDDI_ALLOCATIONLIST</a>
</dt>
<dt>
<a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicecallbacks.md">D3DDDI_DEVICECALLBACKS</a>
</dt>
<dt>
<a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_patchlocationlist.md">D3DDDI_PATCHLOCATIONLIST</a>
</dt>
<dt>
<a href="..\dxgiddi\ns-dxgiddi-dxgi_ddi_base_args.md">DXGI_DDI_BASE_ARGS</a>
</dt>
<dt>
<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_createdevice.md">DxgkDdiCreateDevice</a>
</dt>
<dt>
<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_retrievesubobject.md">RetrieveSubObject(D3D11_1)</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3D10DDIARG_CREATEDEVICE structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>