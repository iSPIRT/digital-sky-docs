# List All applications for user

API to list all applications for current user

**URL** : `/api/user/applications`

**Method** : `GET`

**Auth required** : YES

**Headers** : authentication: Bearer Token

## Success Response

**Code** : `200 OK`

**Content example**

```json
[{
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
	"approverComments": null
}]
```




