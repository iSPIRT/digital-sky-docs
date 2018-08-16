# Login

API to get authentication token for a registered user.

**URL** : `/api/auth/token`

**Method** : `POST`

**Auth required** : NO

**Headers** : application/json

**Data constraints**

```json
{
    "username": "[valid email address]",
    "password": "[password in plain text]"
}
```

**Data example**

```json
{
    "username": "sample@digitalsky.com",
    "password": "abcd1234"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "accessToken": "eyJhbGciOiJSUzI1NiJ9.eyJzdWIiOiIxIiwiaWF0IjoxNTMzNzkyODI5LCJleHAiOjE1MzYzODQ4Mjl9.T584XtKOav0ayHh55sbdj4egCvYLR1dB0T-1VizujpC1KRnNFWsDoidArWj1sKI7fCbLCnvmZHva9bMHJr17RldUNO3jzGoalScjZDd-Svj2kBh4R_Y5kdfY_hveU9xy5xqza-gwoy-v8-aRY_6J4HiqrFBOO9-MCW_4Xv0Ds09XuK7oBkGY2c7g-tLVElSK-jy9Pn6iuvrwgOrXq1UYYA0UFg3z_1K8oQKxPSsLHEdk8iweI3kAvcZHAIkmSTNKSggSKFJGPjS0nHOSzBovIpgL6URflRd-7N8pkJ3JrKRwhvSnp2XDOzcpzoyrRbt_L9gL255xcB_4QfQjlAW-Uw",
    "id": 1,
    "username": "sample",
    "pilotProfileId": 0,
    "individualOperatorProfileId": 0,
    "organizationOperatorProfileId": 0,
    "tokenType": "Bearer",
    "isAdmin": false
}
```

## Error Response

**Condition** : If 'username' and 'password' combination is wrong.

**Code** : `401 UNAUTHORIZED`

**Content** :

```json
{
    "errors": [
        "Invalid email or password"
    ]
}
```