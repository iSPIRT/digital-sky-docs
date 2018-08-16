# Organization Operator Profile Edit

API to edit Organization Operator profile for a registered user

**URL** : `/api/orgOperator/<id>`

**Method** : `PUT`

**Auth required** : YES,

**Headers** : application/json, authentication: Bearer Token

**Data constraints**

```json
{
	"name": "[Valid Name with alphabets and space]",
	"email": "[Valid Organization email id]",
	"mobileNumber": "[Valid mobile number]",
	"contactNumber": "[Valid Organization Landline number]",
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
	"name": "Digitalsky",
	"mobileNumber": "9880098880",
	"contactNumber": "080-456677888",
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


