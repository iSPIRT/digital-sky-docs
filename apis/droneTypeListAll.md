# Drone Type/Model List All

API to list all drone Types

**URL** : `/api/droneType/getAll`

**Method** : `GET`

**Auth required** : YES

**Headers** : application/json, authentication: Bearer Token

## Success Response

**Code** : `200 OK`

**Content example**

```json
[{
  "id": 8,
  "modelName": "Beebop",
  "createdBy": 2,
  "createdDate": "23-08-2018",
  "lastModifiedBy": 2,
  "lastModifiedDate": "23-08-2018",
  "manufacturer": "Beebop",
  "manufacturerAddress": {
    "type": "DEFAULT",
    "lineOne": "House No",
    "lineTwo": "Street",
    "city": "Bangalore",
    "state": "Karnataka",
    "country": "India",
    "pinCode": "56089"
  },
  "manufacturerNationality": "Indian",
  "modelNo": "3222",
  "serialNo": "00001",
  "dateOfManufacture": "08-08-2008",
  "yearOfManufacture": null,
  "wingType": "Fixed",
  "maxTakeOffWeight": 400.0,
  "maxHeightAttainable": 500.0,
  "droneCategoryType": "MEDIUM",
  "compatiblePayload": "payload",
  "purposeOfOperation": "Recreational",
  "proposedBaseOfOperation": "Bangalore",
  "engineType": "Engine Type II",
  "enginePower": 4000.0,
  "engineCount": 2,
  "fuelCapacity": 4000.0,
  "propellerDetails": "some details",
  "dimensions": {
    "length": 4000.0,
    "breadth": 5000.0,
    "height": 1000.0
  },
  "maxEndurance": 300,
  "maxRange": 5000.0,
  "maxSpeed": 400.0,
  "hasGNSS": false,
  "maxHeightOfOperation": 1500.0,
  "opManualDocName": null,
  "maintenanceGuidelinesDocName": null
}]
```

