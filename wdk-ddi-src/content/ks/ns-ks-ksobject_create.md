---
UID : NS:ks.KSOBJECT_CREATE
title : KSOBJECT_CREATE
author : windows-driver-content
description : The KSOBJECT_CREATE structure contains an array of create handlers for base object classes supported by this device object.
old-location : stream\ksobject_create.htm
old-project : stream
ms.assetid : b59d76eb-77c2-4ae5-8be2-f987d7f58446
ms.author : windowsdriverdev
ms.date : 1/9/2018
ms.keywords : KSOBJECT_CREATE, *PKSOBJECT_CREATE, KSOBJECT_CREATE
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : ks.h
req.include-header : Ks.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : KSOBJECT_CREATE
req.alt-loc : ks.h
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
req.typenames : "*PKSOBJECT_CREATE, KSOBJECT_CREATE"
---

# KSOBJECT_CREATE structure
The KSOBJECT_CREATE structure contains an array of create handlers for base object classes supported by this device object.

## Syntax
````
typedef struct {
  ULONG                 CreateItemsCount;
  PKSOBJECT_CREATE_ITEM CreateItemsList;
} KSOBJECT_CREATE, *PKSOBJECT_CREATE;
````

## Members

        
            `CreateItemsCount`

            Contains the number of items in the following array.
        
            `CreateItemsList`

            Points to an array of <a href="..\ks\ns-ks-ksobject_create_item.md">KSOBJECT_CREATE_ITEM</a> structures for base object classes supported by this device object.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | ks.h (include Ks.h) |

    ## See Also

        <dl>
<dt>
<a href="..\ks\ns-ks-ksobject_create_item.md">KSOBJECT_CREATE_ITEM</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSOBJECT_CREATE structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>