---
UID : NS:gnssdriver.GNSS_GEOFENCE_ALERT_DATA
title : GNSS_GEOFENCE_ALERT_DATA
author : windows-driver-content
description : This structure is used by the GNSS engine to notify a geofence breach alert.
old-location : sensors\gnss_geofence_alert_data.htm
old-project : sensors
ms.assetid : 4F7CBB1C-6D23-4015-8403-ABD06B9DC337
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : GNSS_GEOFENCE_ALERT_DATA, GNSS_GEOFENCE_ALERT_DATA, *PGNSS_GEOFENCE_ALERT_DATA
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : gnssdriver.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : GNSS_GEOFENCE_ALERT_DATA
req.alt-loc : gnssdriver.h
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
req.typenames : GNSS_GEOFENCE_ALERT_DATA, *PGNSS_GEOFENCE_ALERT_DATA
---

# GNSS_GEOFENCE_ALERT_DATA structure
This structure is used by the GNSS engine to notify a geofence breach alert.

## Syntax
````
typedef struct {
  ULONG                 Size;
  ULONG                 Version;
  ULONG                 GeofenceID;
  GNSS_GEOFENCE_STATE   GeofenceState;
  GNSS_FIXDATA_BASIC    FixBasicData;
  GNSS_FIXDATA_ACCURACY FixAccuracyData;
  BYTE                  Unused[512];
} GNSS_GEOFENCE_ALERT_DATA, *PGNSS_GEOFENCE_ALERT_DATA;
````

## Members

        
            `FixAccuracyData`

            The fix used to determine the geofence breach. Instead of the full set of fix data, a smaller subset contained in this field and the  FixBasicData field is expected.
        
            `FixBasicData`

            The fix used to determine the geofence breach. Instead of the full set of fix data, a smaller subset contained in this field and the  FixAccuracyData field is expected.
        
            `GeofenceID`

            The ID of the geofence. This ID was generated by the GNSS engine during creation of the geofence.
        
            `GeofenceState`

            The new state of the geofence. The alert implies transitioning to this state.
        
            `Size`

            Structure size.
        
            `Version`

            Version number.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | gnssdriver.h |