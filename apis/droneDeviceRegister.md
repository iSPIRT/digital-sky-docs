# Drone Device Register

API for drones to register

**URL** : `/api/droneDevice/register/<manufacturerBusinessIdentifier>`

**Method** : `POST`

**Auth required** : NO,

**Headers** : application/json

**Data constraints**

```json
{
  "drone" : {
	"version" : "[version of api as string and is mandatory]",
	"txn": "[transaction identifier (mandatory string attribute of max length 50) entered by manufacturer, which is also 		returned as part of response as is and is useful for linking transactions full round trip across systems]",
	"deviceId": "[Unique Drone Device Id which is a mandatory string attribute]",
	"deviceModelId": "[mandatory attribute of type string]",
	"operatorBusinessIdentifier" : "[Operator Unique identifier to be linked to the drone device which is mandatory string		attributeof max length 36]",
	"idHash" : "[optional string attribute]",
	},
"signature" : "[Base64 Encoded Digital Signature(SHA256withRSA signed)of the drone data and is a mandatory string attribute]" ,
"digitalCertificate" : "[Base64 Encoded X509 Certificate of the manufacturer and is a mandatory string attribute]"
}
```

## Response

**Code** : `201 CREATED`

```json

{	
   "txn": "[transaction identifier as entered in the request]",
   "responseTimeStamp": "",
   "code": "[ one of REGISTERED, REGISTRATION_FAILED, OPERATOR_BUSINESS_IDENTIFIER_INVALID,   	
   		OPERATOR_BUSINESS_IDENTIFIER_MISSING, INVALID_SIGNATURE, INVALID_DIGITAL_CERTIFICATE, 					DRONE_ALREADY_REGISTERED, INVALID_MANUFACTURER, MANUFACTURER_BUSINESS_IDENTIFIER_INVALID,	  			BAD_REQUEST_PAYLOAD]",
   "error": "[details of error]"
}

```

## Error Response

**Condition** : If provided with invalid payload, missing mandatory attributes, invalid digital signature, operator business identifier missing, operator
business identifier does not match with any operator in the system, manufacturer business identifier in the url is invalid, manufacturer organisation name in the digital certificate is not matching with that
of the subject name in the digital certificate sent as a part of payload, invalid digital certificate sent as part of payload,
invalid/missing manufacturer intermediate/trusted digital certificate chain, drone is already registered with the unique device 
identifier

**Code** : `400 BAD REQUEST`


