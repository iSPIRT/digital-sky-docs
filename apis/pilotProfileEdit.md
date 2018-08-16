# Pilot Profile Edit

API to edit pilot profile for a registered user

**URL** : `/api/pilot/<id>`

**Method** : `PUT`

**Auth required** : YES,

**Headers** : application/json, authentication: Bearer Token

**Data constraints**

```json
{
	"name": "[Valid Name with alphabets and space]",
	"mobileNumber": "[Valid mobile number]",
	"dateOfBirth": "[Date of birth in dd-MM-yyyy format]",
	"country": "[Valid Country as String]",
	"addressList": [{
		"lineOne": "[Valid Line One as String]",
		"lineTwo": "[Valid Line Two as String]",
		"city": "[Valid City as String]",
		"state": "[Valid State as String]",
		"country":"[Valid Country as String]",
		"pinCode": "[Valid PinCode as String]",
	}]
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "id": 1,
	"name": "Sample",
	"mobileNumber": "9880098880",
	"dateOfBirth": "12-12-1981",
	"country": "India",
	"addressList": [{
		"lineOne": "#25, xyz Building",
		"lineTwo": "Sample",
		"city": "Bangalore",
		"state": "Karnataka",
		"country":"India",
		"pinCode": "560001",
	}]
}
```

## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`


