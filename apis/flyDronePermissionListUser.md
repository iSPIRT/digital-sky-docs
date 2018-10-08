# Fly Drone Permission Applications List for current user

API to list all Fly Drone Permission applications for current user

**URL** : `/api/applicationForm/flyDronePermissionApplication/list?droneId=?`

**Method** : `GET`

**Auth required** : YES

**Headers** : authentication: Bearer Token

## Success Response

**Code** : `200 OK`

**Content example**

```json
[{
 	"id":1,
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
 	"pilotBusinessIdentifier": "1234",
 	"flyArea": [{
 		"latitude": 1.0,
 		"longitude": 1.0
 	}, {
 		"latitude": 2.0,
 		"longitude": 2.0
 	}],
 	"droneId": 1,
 	"payloadWeightInKg": 12.0,
 	"payloadDetails": "test",
 	"flightPurpose": "test",
 	"startDateTime": "18-07-2018 00:00:00",
 	"endDateTime": "18-07-2018 01:00:00",
 	"recurringTimeExpression": "0 0 0 ? * 1#1 *",
 	"recurringTimeDurationInMinutes": 60,
 	"recurringTimeExpressionType": "CRON_QUARTZ"
 }]
```




