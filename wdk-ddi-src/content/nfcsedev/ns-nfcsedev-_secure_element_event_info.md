---
UID : NS:nfcsedev._SECURE_ELEMENT_EVENT_INFO
title : _SECURE_ELEMENT_EVENT_INFO
author : windows-driver-content
description : This structure provides information about a secure element event.
old-location : nfpdrivers\secure_element_event_info.htm
old-project : nfpdrivers
ms.assetid : 72B31C26-89D3-49B2-A404-E6F096D0A334
ms.author : windowsdriverdev
ms.date : 12/18/2017
ms.keywords : _SECURE_ELEMENT_EVENT_INFO, *PSECURE_ELEMENT_EVENT_INFO, SECURE_ELEMENT_EVENT_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : nfcsedev.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : SECURE_ELEMENT_EVENT_INFO
req.alt-loc : nfcsedev.h
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
req.typenames : "*PSECURE_ELEMENT_EVENT_INFO, SECURE_ELEMENT_EVENT_INFO"
---

# _SECURE_ELEMENT_EVENT_INFO structure
This structure provides information about a secure element event.

## Syntax
````
typedef struct _SECURE_ELEMENT_EVENT_INFO {
  GUID                                     guidSecureElementId;
  SECURE_ELEMENT_EVENT_TYPE                eEventType;
  DWORD                                    cbEventData;
  _Field_size_bytes_(cbEventData)
    BYTE pbEventData[ANYSIZE_ARRAY];
} SECURE_ELEMENT_EVENT_INFO, *PSECURE_ELEMENT_EVENT_INFO;
````

## Members

        
            `cbEventData`

            This is the amount of bytes for the pbEventData array.
        
            `eEventType`

            This is an event type. For more information about the types, see the <a href="..\nfcsedev\ne-nfcsedev-_secure_element_event_type.md">SECURE_ELEMENT_EVENT_TYPE</a> enumeration topic.
        
            `guidSecureElementId`

            This is a unique identifier for the secure element.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | nfcsedev.h |