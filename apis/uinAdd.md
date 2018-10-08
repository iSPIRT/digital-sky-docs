# UIN Application Add

API to create UIN application

**URL** : `/api/applicationForm/uinApplication`

**Method** : `POST`

**Auth required** : YES,

**Headers** : multipart/form-data, authentication: Bearer Token

**Form Data**

| Name                       | Value                              |
| ---------------------------|------------------------------------|
| uinApplication             | json string                        |
| importPermissionDoc        | file upload                        |
| cinDoc                     | file upload                        |
| gstinDoc                   | file upload                        |
| panCardDoc                 | file upload                        |
| dotPermissionDoc           | file upload                        |
| securityClearanceDoc       | file upload                        |
| etaDoc                     | file upload                        |
| opManualDoc                | file upload                        |
| maintenanceGuidelinesDoc   | file upload                        |


** uinApplication**

```json
{
  "feeDetails": "[valid string]",
  "droneTypeId": "[drone type id of type long obtained from selected drone saved in the system]",
  "operatorDroneId": "[operator drone id of type long obtained from drone details saved in the system]",
  "manufacturer": "[manufacturer of selected drone of type string obtained from drone details saved in the system]",
  "manufacturerAddress": "[manufacturer address of selected drone obtained from drone details saved in the system]",
  "manufacturerNationality": "[manufacturer nationality of selected drone obtained from drone details saved in the system]",
  "modelName": "[model name of selected drone obtained from drone details saved in the system of type string]",
  "modelNo": "[model no of selected drone obtained from drone details saved in the system of type string]",
  "serialNo": "[serial no of selected drone obtained from drone details saved in the system of type string]",
  "dateOfManufacture": "[date of manufacture of selected drone obtained from drone details saved in the system]",
  "wingType": "[wingType property of the selected drone which is an enum [FIXED, ROTARY]]",
  "maxTakeOffWeight": "[maxTakeOffWeight property of the selected drone as float]",
  "maxHeightAttainable": "[maxHeightAttainable property of the selected drone as float]",
  "compatiblePayload": "[compatiblePayload property of the selected drone as string]",
  "droneCategoryType": "[droneCategory property of the selected drone which is one of [MICRO, SMALL, MEDIUM, LARGE]",
  "purposeOfOperation": "[purposeOfOperation property of the seleced drone as string]",
  "engineType": "[engineType property of selected drone as string]",
  "enginePower": "[enginePower property of selected drone as float]",
  "engineCount": "[engineCount property of selected drone as int]",
  "fuelCapacity": "[fuelCapacity property of selected drone as float]",
  "propellerDetails": "[propellerDetails property of selected drone as string]",
  "maxEndurance": "[max endurance property of selected drone as float]",
  "maxRange": "[max range property of selected drone as float]",
  "maxSpeed": "[max speed property of selected drone as float]",
  "maxHeightOfOperation": "[max height property of selected drone as float]",
  "dimensions": {
    "length": "[length of selected drone as float]",
    "breadth": "[breadth of selected drone as float]",
    "height": "[height of selected drone as float]"
  }
}
```


## Success Response

**Code** : `200 OK`

**Content example**

```json
{
  "id": "5b7e70f2e5a4c9089e1506ea",
  "createdDate": "23-08-2018",
  "applicationNumber": null,
  "applicant": "operatora",
  "applicantId": 1,
  "applicantAddress": null,
  "applicantEmail": null,
  "applicantPhone": null,
  "applicantNationality": null,
  "applicantType": null,
  "submittedDate": null,
  "lastModifiedDate": null,
  "status": "DRAFT",
  "approver": null,
  "approverId": 0,
  "approvedDate": null,
  "approverComments": null,
  "importPermissionDocName": "importPermissionDoc.jpg",
  "cinDocName": "cinDoc.jpg",
  "gstinDocName": "gstinDoc.jpg",
  "panCardDocName": null,
  "securityClearanceDocName": "securityClearanceDoc.jpg",
  "dotPermissionDocName": "dotPermissionDoc.jpg",
  "etaDocName": "etaDoc.jpg",
  "feeDetails": "By Cheque ending 4899 from SBI",
  "droneTypeId": 1,
  "operatorDroneId": 11,
  "manufacturer": "Beebop",
  "manufacturerId": 0,
  "manufacturerAddress": {
    "lineOne": "House No",
    "lineTwo": "",
    "city": "Bangalore",
    "state": "Karnataka",
    "country": "India",
    "pinCode": 560078
  },
  "manufacturerNationality": "a",
  "modelName": "BEEPOP",
  "modelNo": "99",
  "serialNo": "2",
  "dateOfManufacture": "01-01-2009",
  "wingType": "Rotary",
  "isNew": true,
  "maxTakeOffWeight": 4.0,
  "maxHeightAttainable": 5.0,
  "compatiblePayload": "7",
  "droneCategoryType": "MEDIUM",
  "regionOfOperation": null,
  "purposeOfOperation": "9",
  "engineType": "some type",
  "enginePower": 8000.0,
  "engineCount": 2,
  "fuelCapacity": 8000.0,
  "propellerDetails": "details",
  "dimensions": {
    "length": 4000.0,
    "breadth": 2000.0,
    "height": 1000.0
  },
  "maxEndurance": 4,
  "maxRange": 5000.0,
  "maxSpeed": 5000.0,
  "maxHeightOfOperation": 1000.0,
  "opManualDocName": null,
  "maintenanceGuidelinesDocName": null,
  "incidentHistory": null
}
```

## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`
