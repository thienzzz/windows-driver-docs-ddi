---
UID : NS:ucmtcpciportcontroller._UCMTCPCI_PORT_CONTROLLER_ALERT_DATA
title : _UCMTCPCI_PORT_CONTROLLER_ALERT_DATA
author : windows-driver-content
description : Contains information about hardware alerts received on the port controller object. This structure is used in the UcmTcpciPortControllerAlert call. Call UCMTCPCI_PORT_CONTROLLER_ALERT_DATA_INIT to initialize this structure.
old-location : buses\ucmtcpci_port_controller_alert_data.htm
old-project : usbref
ms.assetid : 4b3c2fc8-d7c3-4223-a88e-5db9ad852618
ms.author : windowsdriverdev
ms.date : 1/4/2018
ms.keywords : _UCMTCPCI_PORT_CONTROLLER_ALERT_DATA, *PUCMTCPCI_PORT_CONTROLLER_ALERT_DATA, UCMTCPCI_PORT_CONTROLLER_ALERT_DATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ucmtcpciportcontroller.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : UCMTCPCI_PORT_CONTROLLER_ALERT_DATA
req.alt-loc : ucmtcpciportcontroller.h
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
req.typenames : "*PUCMTCPCI_PORT_CONTROLLER_ALERT_DATA, UCMTCPCI_PORT_CONTROLLER_ALERT_DATA"
req.product : Windows 10 or later.
---

# _UCMTCPCI_PORT_CONTROLLER_ALERT_DATA structure
Contains information about hardware alerts received on the port controller object. This structure is used in the <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrolleralert.md">UcmTcpciPortControllerAlert</a> call. Call <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpci_port_controller_alert_data_init.md">UCMTCPCI_PORT_CONTROLLER_ALERT_DATA_INIT</a> to initialize this structure.

## Syntax
````
typedef struct _UCMTCPCI_PORT_CONTROLLER_ALERT_DATA {
  ULONG                               Size;
  UCMTCPCI_PORT_CONTROLLER_ALERT_TYPE AlertType;
  union {
    UCMTCPCI_PORT_CONTROLLER_CC_STATUS       CCStatus;
    UCMTCPCI_PORT_CONTROLLER_POWER_STATUS    PowerStatus;
    UCMTCPCI_PORT_CONTROLLER_FAULT_STATUS    FaultStatus;
    PUCMTCPCI_PORT_CONTROLLER_RECEIVE_BUFFER ReceiveBuffer;
  };
} UCMTCPCI_PORT_CONTROLLER_ALERT_DATA, *PUCMTCPCI_PORT_CONTROLLER_ALERT_DATA;
````

## Members

        
            `AlertType`

            A <a href="..\ucmtcpciportcontroller\ne-ucmtcpciportcontroller-_ucmtcpci_port_controller_alert_type.md">UCMTCPCI_PORT_CONTROLLER_ALERT_TYPE</a> value that indicates the type of hardware alert.
        
            `Size`

            Size of this structure.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ucmtcpciportcontroller.h |

    ## See Also

        <dl>
<dt>
<a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrolleralert.md">UcmTcpciPortControllerAlert</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [usbref\buses]:%20UCMTCPCI_PORT_CONTROLLER_ALERT_DATA structure%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>