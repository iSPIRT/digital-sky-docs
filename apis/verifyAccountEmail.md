# Verify Account Email

API to validate email id of a registered user.

**URL** : `/api/user/verify`

**Method** : `POST`

**Auth required** : NO

**Headers** : application/json

**Data constraints**

```json
{
    "token": "[verification token sent to registered email]"
}
```

## Success Response

**Code** : `200 OK`


## Error Response

**Condition** : If provided with invalid token.

**Code** : `404 NOT FOUND`

