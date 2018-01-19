---
UID : NE:wwan._WWAN_ASYNC_GETSET_TYPE
title : _WWAN_ASYNC_GETSET_TYPE
author : windows-driver-content
description : The WWAN_ASYNC_GETSET_TYPE enumeration lists the different asynchronous OID get/set requests.
old-location : netvista\wwan_async_getset_type.htm
old-project : netvista
ms.assetid : 2FECDA17-7B38-4636-AFAF-D923AECFAF68
ms.author : windowsdriverdev
ms.date : 1/11/2018
ms.keywords : _WWAN_ASYNC_GETSET_TYPE, *PWWAN_ASYNC_GETSET_TYPE, WWAN_ASYNC_GETSET_TYPE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : enum
req.header : wwan.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : Supported starting with  Windows 8.
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : WWAN_ASYNC_GETSET_TYPE
req.alt-loc : wwan.h
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
req.typenames : "*PWWAN_ASYNC_GETSET_TYPE, WWAN_ASYNC_GETSET_TYPE"
req.product : Windows 10 or later.
---

# _WWAN_ASYNC_GETSET_TYPE Enumeration
The WWAN_ASYNC_GETSET_TYPE enumeration lists the different asynchronous OID get/set requests.

## Syntax
````
typedef enum _WWAN_ASYNC_GETSET_TYPE { 
  WwanAsyncGetDeviceCaps                         = 0,
  WwanAsyncGetReadyInfo                          = ,
  WwanAsyncGetRadioState                         = ,
  WwanAsyncSetRadioState                         = ,
  WwanAsyncGetPin                                = ,
  WwanAsyncSetPin                                = ,
  WwanAsyncGetPinList                            = ,
  WwanAsyncGetHomeProvider                       = ,
  WwanAsyncSetHomeProvider                       = ,
  WwanAsyncGetPreferredProviders                 = ,
  WwanAsyncSetPreferredProviders                 = ,
  WwanAsyncGetVisibleProviders                   = ,
  WwanAsyncGetRegisterState                      = ,
  WwanAsyncSetRegisterState                      = ,
  WwanAsyncGetPacketService                      = ,
  WwanAsyncSetPacketService                      = ,
  WwanAsyncGetSignalState                        = ,
  WwanAsyncSetSignalState                        = ,
  WwanAsyncGetConnect                            = ,
  WwanAsyncSetConnect                            = ,
  WwanAsyncGetProvisionedContexts                = ,
  WwanAsyncSetProvisionedContext                 = ,
  WwanAsyncSetServiceActivation                  = ,
  WwanAsyncGetSmsConfiguration                   = ,
  WwanAsyncSetSmsConfiguration                   = ,
  WwanAsyncSmsRead                               = ,
  WwanAsyncSmsSend                               = ,
  WwanAsyncSmsDelete                             = ,
  WwanAsyncSmsStatus                             = ,
  WwanAsyncSetVendorSpecific                     = ,
  WwanAsyncSetProfileIndex                       = ,
  WwanAsyncGetDeviceServices                     = ,
  WwanAsyncSubscribeDeviceServiceEvents          = ,
  WwanAsyncAuthChallenge                         = ,
  WwanAsyncUssdRequest                           = ,
  WwanAsyncSetPinEx                              = ,
  WwanAsyncGetPinEx get request.                 = ,
  WwanAsyncGetDeviceServiceCommand get request.  = ,
  WwanAsyncSetDeviceServiceCommand               = ,
  WWAN_ASYNC_GETSET_TYPE_MAX                     = 
} WWAN_ASYNC_GETSET_TYPE;
````

## Constants

<table>

<tr>
<td>WWAN_ASYNC_GETSET_TYPE_MAX</td>
<td>The maximum number of entries in the WWAN_ASYNC_GETSET_TYPE enumeration.</td>
</tr>

<tr>
<td>WwanAsyncAuthChallenge</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/hh440092">OID_WWAN_AUTH_CHALLENGE</a></td>
</tr>

<tr>
<td>WwanAsyncGetConnect</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569823">OID_WWAN_CONNECT</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetDeviceCaps</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569824">OID_WWAN_DEVICE_CAPS</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetDeviceServiceCommand</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/hh440094">OID_WWAN_DEVICE_SERVICE_COMMAND</a></td>
</tr>

<tr>
<td>WwanAsyncGetDeviceServices</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/hh440093">OID_WWAN_DEVICE_SERVICES</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetHomeProvider</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569826">OID_WWAN_HOME_PROVIDER</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetPacketService</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569827">OID_WWAN_PACKET_SERVICE</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetPin</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569828">OID_WWAN_PIN</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetPinEx</td>
<td>Asynchronous OID_WWAN_PIN_EX get request.</td>
</tr>

<tr>
<td>WwanAsyncGetPinList</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569829">OID_WWAN_PIN_LIST</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetPreferredProviders</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569830">OID_WWAN_PREFERRED_PROVIDERS</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetProvisionedContexts</td>
<td>Asynchronous <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/oid-wwan-provisioned-contexts">OID_WWAN_PROVISIONED_CONTEXTS</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetRadioState</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569832">OID_WWAN_RADIO_STATE</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetReadyInfo</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569833">OID_WWAN_READY_INFO</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetRegisterState</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569834">OID_WWAN_REGISTER_STATE</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetSignalState</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569836">OID_WWAN_SIGNAL_STATE</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetSmsConfiguration</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569837">OID_WWAN_SMS_CONFIGURATION</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncGetVisibleProviders</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569843">OID_WWAN_VISIBLE_PROVIDERS</a> get request.</td>
</tr>

<tr>
<td>WwanAsyncSetConnect</td>
<td>Asynchronous OID_WWAN_CONNECT set request.</td>
</tr>

<tr>
<td>WwanAsyncSetDeviceServiceCommand</td>
<td>Asynchronous OID_WWAN_DEVICE_SERVICE_COMMAND set request.</td>
</tr>

<tr>
<td>WwanAsyncSetHomeProvider</td>
<td>Asynchronous OID_WWAN_HOME_PROVIDER set request.</td>
</tr>

<tr>
<td>WwanAsyncSetPacketService</td>
<td>Asynchronous OID_WWAN_PACKET_SERVICE set request.</td>
</tr>

<tr>
<td>WwanAsyncSetPin</td>
<td>Asynchronous OID_WWAN_PIN set request.</td>
</tr>

<tr>
<td>WwanAsyncSetPinEx</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/hh440095">OID_WWAN_PIN_EX</a> set request.</td>
</tr>

<tr>
<td>WwanAsyncSetPreferredProviders</td>
<td>Asynchronous OID_WWAN_PREFERRED_PROVIDERS set request.</td>
</tr>

<tr>
<td>WwanAsyncSetProfileIndex</td>
<td>Reserved.</td>
</tr>

<tr>
<td>WwanAsyncSetProvisionedContext</td>
<td>Asynchronous OID_WWAN_PROVISIONED_CONTEXTS set request.</td>
</tr>

<tr>
<td>WwanAsyncSetRadioState</td>
<td>Asynchronous OID_WWAN_RADIO_STATE set request.</td>
</tr>

<tr>
<td>WwanAsyncSetRegisterState</td>
<td>Asynchronous OID_WWAN_REGISTER_STATE set request.</td>
</tr>

<tr>
<td>WwanAsyncSetServiceActivation</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569835">OID_WWAN_SERVICE_ACTIVATION</a> set request.</td>
</tr>

<tr>
<td>WwanAsyncSetSignalState</td>
<td>Asynchronous OID_WWAN_SIGNAL_STATE set request.</td>
</tr>

<tr>
<td>WwanAsyncSetSmsConfiguration</td>
<td>Asynchronous OID_WWAN_SMS_CONFIGURATION set request.</td>
</tr>

<tr>
<td>WwanAsyncSetVendorSpecific</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569842">OID_WWAN_VENDOR_SPECIFIC</a></td>
</tr>

<tr>
<td>WwanAsyncSmsDelete</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569838">OID_WWAN_SMS_DELETE</a></td>
</tr>

<tr>
<td>WwanAsyncSmsRead</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569839">OID_WWAN_SMS_READ</a></td>
</tr>

<tr>
<td>WwanAsyncSmsSend</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569840">OID_WWAN_SMS_SEND</a></td>
</tr>

<tr>
<td>WwanAsyncSmsStatus</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/ff569841">OID_WWAN_SMS_STATUS</a></td>
</tr>

<tr>
<td>WwanAsyncSubscribeDeviceServiceEvents</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/hh440096">OID_WWAN_SUBSCRIBE_DEVICE_SERVICE_EVENTS</a></td>
</tr>

<tr>
<td>WwanAsyncUssdRequest</td>
<td>Asynchronous <a href="https://msdn.microsoft.com/library/windows/hardware/hh440100">OID_WWAN_USSD</a></td>
</tr>
</table>


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | wwan.h |

## See Also

<dl>
<dt>
<a href="https://msdn.microsoft.com/922b6b55-c332-4721-bbd1-571b0e154df3">MB Data Model</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [netvista\netvista]:%20WWAN_ASYNC_GETSET_TYPE enumeration%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>