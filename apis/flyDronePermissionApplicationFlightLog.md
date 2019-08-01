# Drone Type/Model Add

API for admin to create drone type/model

**URL** : `/api/applicationForm/flyDronePermissionApplication/<id>//document/flightLog`

**Method** : `POST`

**Auth required** : YES,

**Headers** : application/json, authentication: Bearer Token

**Data constraints**

**MultipartFile**: `flightLogDocument`

```json
{
    "PermissionArtefact": {
                            "type": "string",
                            "title": "Permission Artefact ID",
                            "description": "The ID of the current permission artefact against which the log is being generated. "},
    "previous_log_hash":{
                            "$id": "#/properties/FlightLog/properties/previous_log_hash",
                            "type": "string",
                            "title": "The Previous Log hash",
                            "description": "This contains the base64 encoded hash of the most recent flight log that was generated",
                            "default": "" },
    "LogEntries": {
              "type": "array",
              "title": "The Logentries Schema",
              "items": {
                "type": "object",
                "title": "Flight Log items",
                "required": [
                  "Entry_type",
                  "TimeStamp",
                  "Longitude",
                  "Latitude",
                  "Altitude"
                ],
                "properties": {
                  "Entry_type": {
                    "type": "string",
                    "enum": [
                      "GEOFENCE_BREACH",
                      "TAKEOFF/ARM",
                      "TIME_BREACH",
                      "LAND/DISARM"
                    ],
                    "title": "Flight Log entries",
                    "description": "Every entry in the flight log should be one of the four types"
                  },
                  "TimeStamp": {
                    "type": "integer",
                    "title": "Unix timestamp of the recorded entry",
                    "default": 0
                  },
                  "Longitude": {
                    "type": "number",
                    "title": "The Longitude in decimal Degrees",
                    "default": 0,
                    "examples": [
                      12.34567
                    ]
                  },
                  "Latitude": {
                    "type": "number",
                    "title": "The Latitude in decimal degrees",
                    "default": 0.0,
                    "examples": [
                      12.34567
                    ]
                  },
                  "Altitude": {
                    "type": "number",
                    "title": "The ellipsoidal height in m",
                    "default": 0,
                    "examples": [
                      100.1
                    ]
                  },
                  "CRC": {
                    "type": "integer",
                    "title": "The Crc Schema (Optional)",
                    "default": 0,
                    "examples": [
                      719
                    ]
                  }
                }
              }
            }
}
```

## Success Response

**Code** : `200 OK`

**Content example** : `empty object`
```
{}
```
## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`


