# Register

API to register user.

**URL** : `/api/user`

**Method** : `POST`

**Auth required** : NO

**Headers** : application/json

**Data constraints**

```json
{
	"fullName":"[Valid Name alphabets+space]",
	"email":"[Valid Email]",
	"password":"[Password with minimum length of 8]",
	"reCaptcha": "[Valid reCaptcha]""
}
```

**Data example**

```json
{
	"fullName":"Sample Name",
	"email":"sample@digitalsky.com",
	"password":"password",
	"reCaptcha": "64239jhvasjajddjf"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "id": 1
}
```

## Error Response

**Condition** : If invalid payload.

**Code** : `400 BAD REQUEST`

