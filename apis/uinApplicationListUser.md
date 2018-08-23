# UIN Applications List for current user

API to list all UIN applications for current user

**URL** : `/api/applicationForm/uinApplication/list`

**Method** : `GET`

**Auth required** : YES

**Headers** : authentication: Bearer Token

## Success Response

**Code** : `200 OK`

**Content example**

```json
[{
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
  "submittedDate": "23-08-2018",
  "lastModifiedDate": "23-08-2018",
  "status": "APPROVED",
  "approver": "admin",
  "approverId": 2,
  "approvedDate": "23-08-2018",
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
    "pinCode": "560078"
  },
  "manufacturerNationality": "Indian",
  "modelName": "BEEPOP",
  "modelNo": "99",
  "serialNo": "2",
  "dateOfManufacture": "01-01-2009",
  "wingType": "Rotary",
  "isNew": true,
  "maxTakeOffWeight": 1000.0,
  "maxHeightAttainable": 1500.0,
  "compatiblePayload": "details",
  "droneCategoryType": "MEDIUM",
  "regionOfOperation": null,
  "purposeOfOperation": "educational",
  "engineType": "type",
  "enginePower": 4000.0,
  "engineCount": 2,
  "fuelCapacity": 8000.0,
  "propellerDetails": "details",
  "dimensions": {
    "length": 5000.0,
    "breadth": 2000.0,
    "height": 1000.0
  },
  "maxEndurance": 4,
  "maxRange": 5000.0,
  "maxSpeed": 4000.0,
  "maxHeightOfOperation": 1500.0,
  "previousUIN": null,
  "opManualDocName": "opManualDoc.jpg",
  "maintenanceGuidelinesDocName": "maintenanceGuidelinesDoc.jpg",
  "incidentHistory": "No History"
}]
```




