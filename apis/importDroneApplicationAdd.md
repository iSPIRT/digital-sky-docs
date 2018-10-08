# Import Drone Application Add

API to create import Drone application

**URL** : `/api/applicationForm/importDroneApplication`

**Method** : `POST`

**Auth required** : YES,

**Headers** : application/json, authentication: Bearer Token

**Form Data**

| Name                       | Value                              |
| ---------------------------|------------------------------------|
| acquisitionForm        | json string                        |


** acquisitionForm**

```json
{
  "applicant": "[logged in user's name as string]",
  "applicantAddress": "[logged in user's address]",
  "applicantNationality": "[logged in user's nationality as string]",
  "droneTypeId": "[id of dronetype selected as long]",
  "manufacturer": "[manufacturer property of selected drone as string]",
  "manufacturerNationality": "[nationality property of the manufacturer of selected drone as string]",
  "manufacturerAddress": "[manufacturer address property of the selected drone]",
  "modelName": "[modelName property of the selected drone as string]",
  "modelNo": "[modelNo property of the selected drone as string]",
  "serialNo": "[serialNo property of the selected drone as string]",
  "dateOfManufacture": "[dateOfManufacture property of the selected drone as date]",
  "wingType": "[wingType property of the selected drone which is an enum [FIXED, ROTARY]]",
  "maxTakeOffWeight": "[maxTakeOffWeight property of the selected drone as float]",
  "maxHeightAttainable": "[maxHeightAttainable property of the selected drone as float]",
  "noOfDrones": "[valid number]"
}
```


## Success Response

**Code** : `200 OK`

**Content example**

```json
{
  "id": "5b7be786e5a4c9089e1506e9",
  "createdDate": "21-08-2018",
  "applicationNumber": null,
  "applicant": "operatora",
  "applicantId": 1,
  "applicantAddress": {
    "lineOne": "House No:",
    "lineTwo": "Street Name",
    "city": "Bangalore",
    "state": "Karnataka",
    "country": "India",
    "pinCode": "560078"
  },
  "applicantEmail": null,
  "applicantPhone": null,
  "applicantNationality": "Indian",
  "applicantType": null,
  "submittedDate": null,
  "lastModifiedDate": "21-08-2018",
  "status": "DRAFT",
  "approver": null,
  "approverId": 0,
  "approvedDate": null,
  "approverComments": null,
  "manufacturer": "Beebop",
  "manufacturerId": 0,
  "manufacturerAddress": {
    "lineOne": "House No:",
    "lineTwo": "Street Name",
    "city": "Chennai",
    "state": "Tamil Nadu",
    "country": "India",
    "pinCode": "567899"
  },
  "manufacturerNationality": "Indian",
  "droneTypeId": 1,
  "owner": "Owner",
  "ownerId": 0,
  "ownerAddress": {
    "lineOne": "House No:",
    "lineTwo": "Street Name",
    "city": "Bangalore",
    "state": "Karnataka",
    "country": "India",
    "pinCode": "568900"
  },
  "modelName": "BEEBOP",
  "modelNo": "99",
  "serialNo": "2",
  "dateOfManufacture": "01-01-2009",
  "yearOfManufacture": null,
  "wingType": "Rotary",
  "noOfDrones": 2,
  "isNew": true,
  "maxTakeOffWeight": 4.0,
  "maxHeightAttainable": 5.0,
  "compatiblePayload": null,
  "purposeOfOperation": "Educational",
  "proposedBaseOfOperation": "Bangalore",
  "securityClearanceDocName": "securityClearanceDoc.jpg",
  "applicantCategory": null,
  "acquisitionMode": "LEASE"
}
```

## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`
