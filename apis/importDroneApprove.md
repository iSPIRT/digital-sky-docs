# Import Drone Application Approve

API to approve import drone application

**URL** : `/api/applicationForm/importDroneApplication/approve/<id>`

**Method** : `PATCH`

**Auth required** : YES, Admin Only

**Headers** : multipart/json authentication: Bearer Token

** Data**

```json
{
	"status": "[APPROVED/REJECTED]"
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
  "submittedDate": "21-08-2018",
  "lastModifiedDate": "21-08-2018",
  "status": "APPROVED",
  "approver": "admin",
  "approverId": 2,
  "approvedDate": "21-08-2018",
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
  "wingType": "Rotary",
  "noOfDrones": 2,
  "isNew": true,
  "maxTakeOffWeight": 4.0,
  "maxHeightAttainable": 5.0,
  "compatiblePayload": "some payload",
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


