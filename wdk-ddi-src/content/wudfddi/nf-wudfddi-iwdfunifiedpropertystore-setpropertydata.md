---
UID : NF:wudfddi.IWDFUnifiedPropertyStore.SetPropertyData
title : IWDFUnifiedPropertyStore::SetPropertyData method
author : windows-driver-content
description : The SetPropertyData method modifies the current setting of a device property.
old-location : wdf\iwdfunifiedpropertystore_setpropertydata.htm
old-project : wdf
ms.assetid : 07A79E40-6C49-4AF8-90B8-26652C46B6F1
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : IWDFUnifiedPropertyStore, IWDFUnifiedPropertyStore::SetPropertyData, SetPropertyData
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : method
req.header : wudfddi.h
req.include-header : 
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 1.11
req.alt-api : IWDFUnifiedPropertyStore.SetPropertyData
req.alt-loc : WUDFx.dll
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : Unavailable in UMDF 2.0 and later.
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : WUDFx.dll
req.irql : 
req.typenames : "*PPOWER_ACTION, POWER_ACTION"
req.product : Windows 10 or later.
---


# SetPropertyData method
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>SetPropertyData</b> method modifies the current setting of a device property.

## Syntax

````
HRESULT SetPropertyData(
  [in]           const DEVPROPKEY  *PropertyKey,
  [in]                 LCID        Lcid,
  [in]                 ULONG       Flags,
  [in]                 DEVPROPTYPE PropertyType,
  [in]                 ULONG       PropertyDataSize,
  [in, optional]       PVOID       PropertyData
);
````

## Parameters

`PropertyKey`

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn315031">DEVPROPKEY</a> structure that specifies the device property key.

`Lcid`

Specifies a locale identifier. Set this parameter either to a language-specific LCID value or to LOCALE_NEUTRAL. The LOCALE_NEUTRAL LCID specifies that the property is language-neutral (that is, not specific to any language). Do not set this parameter to LOCALE_SYSTEM_DEFAULT or LOCALE_USER_DEFAULT. For more information about language-specific LCID values, see <a href="http://msdn.microsoft.com/en-us/library/cc233968(PROT.10).aspx">LCID Structure</a>.

`Flags`

Reserved. Drivers should set this value to 0.

`PropertyType`

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543546">DEVPROPTYPE</a> value that specifies the type of the data that is provided in the <i>PropertyData</i> buffer.

`PropertyDataSize`

The size, in bytes, of the buffer that <i>PropertyData</i> points to.

`PropertyData`

A pointer to the device property data. Set this parameter to <b>NULL</b> to delete the specified property.


## Return Value

<b>SetPropertyData</b> returns S_OK if the operation succeeds. Otherwise, the method might return the following values.
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>The framework's attempt to allocate memory failed.
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)</b></dt>
</dl>If the driver specifies <b>WdfPropertyStoreRootClassDeviceInterfaceKey</b>, the requested interface must be one that the UMDF driver previously registered.
<dl>
<dt><b>HRESULT_FROM_WIN32 (STATUS_NOT_SUPPORTED)</b></dt>
</dl>The driver can modify device interface property data only  starting with  Windows 8.

 

This method might return an HRESULT-typed value corresponding to one of the other values that <i>Winerror.h</i> contains.

## Remarks

Framework-based drivers use the <b>SetPropertyData</b> method to modify device properties that are defined as part of the unified device property model.

In particular, you can use this method to modify a device's <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-the-registry-in-umdf-1-x-drivers">hardware key</a> or an instance of a device interface class. When you call <a href="https://msdn.microsoft.com/A54E56A6-9A6C-435D-83FD-84BB0E072C74">IWDFUnifiedPropertyStoreFactory::RetrieveUnifiedDevicePropertyStore</a>, set the <i>RootSpecifier</i> parameter's <b>RootClass</b> member to <b>WdfPropertyStoreRootClassHardwareKey</b> or <b>WdfPropertyStoreRootClassDeviceInterfaceKey</b>.  

If you specify  <b>WdfPropertyStoreRootClassHardwareKey</b>, then when you call <b>SetPropertyData</b>, you must provide a custom <a href="https://msdn.microsoft.com/library/windows/hardware/dn315031">DEVPROPKEY</a> value in the <i>PropertyKey</i> parameter, and  not a PnP-defined key. The value must have been previously set by calling <b>SetPropertyData</b>, a <a href="devinst.using_device_installation_functions#ddk_setupdi_device_property_functions_dg#ddk_setupdi_device_property_functions_dg">SetupDI device property function</a>, or by using the <a href="https://msdn.microsoft.com/8fcb1355-f13d-4d96-aa73-62a094a52267">INF AddProperty directive</a>.

If the driver specifies <b>WdfPropertyStoreRootClassDeviceInterfaceKey</b>, the requested interface must be one that the UMDF driver previously registered at runtime.


If the driver registers an interface in its INF file, it must set associated properties in the INF as well.

For more information about accessing the registry, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/using-the-registry-in-umdf-1-x-drivers">Using the Registry in UMDF-based Drivers</a>.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** | 1.11 |
| **Header** | wudfddi.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfunifiedpropertystorefactory.md">IWDFUnifiedPropertyStoreFactory</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451406">RetrieveUnifiedDevicePropertyStore</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfunifiedpropertystore.md">IWDFUnifiedPropertyStore</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451410">GetPropertyData</a>
</dt>
<dt>
<a href="..\wudfddi_types\ns-wudfddi_types-_wdf_property_store_root.md">WDF_PROPERTY_STORE_ROOT</a>
</dt>
<dt>
<a href="..\wudfddi_types\ne-wudfddi_types-_wdf_property_store_root_class.md">WDF_PROPERTY_STORE_ROOT_CLASS</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFUnifiedPropertyStore::SetPropertyData method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>