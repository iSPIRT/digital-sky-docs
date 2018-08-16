# UAOP Application Approve

API to approve UAOP application

**URL** : `/api/applicationForm/uaopApplication/approve/<id>`

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
	"id": "5b75458c4cedfd0005c1b1b5",
	"createdDate": "16-08-2018",
	"applicationNumber": null,
	"applicant": "praveen",
	"applicantId": 1,
	"applicantAddress": null,
	"applicantEmail": null,
	"applicantPhone": null,
	"applicantNationality": null,
	"applicantType": null,
	"submittedDate": null,
	"lastModifiedDate": null,
	"status": "APPROVED",
	"approver": null,
	"approverId": 1,
	"approvedDate": "16-08-2018",
	"approverComments": null,
	"name": "Test",
	"designation": "test123",
	"securityProgramDocName": null,
	"landOwnerPermissionDocName": null,
	"insuranceDocName": null,
	"sopDocName": null
}
```

## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`


