# Generate Reset Password Link

API to generate reset password link for a registered user.

**URL** : `/api/user/resetPasswordLink`

**Method** : `POST`

**Auth required** : NO

**Headers** : application/json

**Data constraints**

```json
{
    "email": "[valid email address]"
}
```

**Data example**

```json
{
    "email": "sample@digitalsky.com"
}
```

## Success Response

**Code** : `201 CREATED`


## Error Response

**Condition** : If provided with incorrect email id.

**Code** : `404 NOT FOUND`

