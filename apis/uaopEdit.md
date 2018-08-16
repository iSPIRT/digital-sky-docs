# UAOP Application Edit

API to edit UAOP application

**URL** : `/api/applicationForm/uaopApplication/<id>`

**Method** : `PATCH`

**Auth required** : YES,

**Headers** : multipart/form-data, authentication: Bearer Token

**Form Data**

| Name                       | Value                              |
| ---------------------------|------------------------------------|
| uaopApplicationForm        | json string                        |
| securityProgramDoc         | file upload                        |
| insuranceDoc               | file upload                        |
| landOwnerPermissionDoc     | file upload                        |
| sopDoc                     | file upload                        |


** uaopApplicationForm**

```json
{
	"name": "[Valid Name with alphabets and space]",
	"designation": "[Valid designation as string]"
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
	"status": "DRAFT",
	"approver": null,
	"approverId": 0,
	"approvedDate": null,
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


