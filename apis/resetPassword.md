# Reset Password

API to reset password for a registered user.

**URL** : `/api/user/resetPassword`

**Method** : `POST`

**Auth required** : NO

**Headers** : application/json

**Data constraints**

```json
{
    "token": "[valid token sent to email]"
}
```


## Success Response

**Code** : `201 CREATED`


## Error Response

**Condition** : If provided with incorrect token.

**Code** : `404 NOT FOUND`

