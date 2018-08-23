# Drone Type/Model Edit

API for admin to create drone type/model

**URL** : `/api/droneType`

**Method** : `PATCH`

**Auth required** : YES,

**Headers** : application/json, authentication: Bearer Token

**Data constraints**

```json
{
  "manufacturer": "[valid manufacturer name as string]",
  "manufacturerAddress": "[manufacturer address of selected drone obtained from drone details saved in the system]",
  "manufacturerNationality": "[valid manufacturer nationality as string]",
  "modelName": "[valid model name as string]",
  "modelNo": "[valid model no as string]",
  "serialNo": "[serial no as string]",
  "dateOfManufacture": "[date of manufacture of [mm-dd-yyyy] format]",
  "wingType": "[wingType which is an enum [FIXED, ROTARY]]",
  "maxTakeOffWeight": "[maxTakeOffWeight  as float]",
  "maxHeightAttainable": "[maxHeightAttainable as float]",
  "compatiblePayload": "[compatiblePayload as string]",
  "droneCategoryType": "[droneCategory which is one of [MICRO, SMALL, MEDIUM, LARGE]]",
  "purposeOfOperation": "[purposeOfOperation as string]",
  "engineType": "[engineType as string]",
  "enginePower": "[enginePower as float]",
  "engineCount": "[engineCount as int]",
  "fuelCapacity": "[fuelCapacity as float]",
  "propellerDetails": "[propellerDetails as string]",
  "maxEndurance": "[max endurance property as float]",
  "maxRange": "[max range property as float]",
  "maxSpeed": "[max speed property as float]",
  "maxHeightOfOperation": "[max height property as float]",
  "dimensions": {
    "length": "[length as float]",
    "breadth": "[breadth as float]",
    "height": "[height as float]"
  }
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
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
}
```

## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`


