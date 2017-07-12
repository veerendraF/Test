#Incoming API

The Incoming API is the gateway that handles all the incoming requests to Empowered Benefits. The Incoming API module currently supports API for the following domains -  Group, Subscriber, Plan and Carriers.

##Group

###Get Group Incoming API –

Retrieves Group information for the specified Group number. If the service is unable to retrieve Group information, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/{partnerCode}
```

###Post Group Incoming API

Creates a new group. If the service is unable to create a new Group, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/{partnerCode}
```

Request payload body :

```
{
  "ebGroupNumber": "ABC123",
  "name": "EB Group Name",
  "primaryContactFirstName": "First Name",
  "primaryContactLastName": "Last Name",
  "primaryContactEmail": "support@empoweredbenefits.com",
  "createAdminID": 123
}
```

###Put Group Incoming API

 Updates information for an existing Group for the specified Group number. If the service is unable to update existing Group information, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/{partnerCode}

```

Request payload body :

```
{
  "name": "EB Group Name",
  "companyStatus": "INACTIVE",
  "billingStartDate": {},
  "billingEndDate": {},
  "createAdminID": 3
}
```

##Subscribers

###Get Subscribers Incoming API

 Retrieves Subscriber information for the specified Subscriber for a specific Group. If the service is unable to retrieve Subscriber information, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/subscribers/{subscriberID}/{partnerCode}

```
###Post Subscribers Incoming API

Creates a new Subscriber within a specified Group. If the service is unable to create a new Subscriber, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/subscribers/{partnerCode}

```

Request payload body :

```
{
  "firstName": "First Name",
  "middleName": "Middle Name",
  "lastName": "Last name",
  "maidenName": "Maiden Name",
  "ssn": "123-45-6789",
  "employeeID": "EMP12345",
  "username": "support@empoweredbenefits.com",
  "gender": "F",
  "hireDate": {},
  "birthDate": {},
  "occupation": "tester579",
  "heightInFeet": 6,
  "heightInInch": 72,
  "weightInPounds": 200,
  "maritalStatus": "MARRIED",
  "tobaccoStatus": "UNDEFINED"
}
```

###Put Subscribers Incoming API

Updates Subscriber information for the specified Subscriber for a specific Group. If the service is unable to update existing Subscriber information, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/subscribers/{subscriberID}/{partnerCode}

```

Request payload body :

```
{
  "subscriberID": 32,
  "firstName": "First Name",
  "middleName": "Middle Name",
  "lastName": "Last name",
  "maidenName": "Maiden Name",
  "ssn": "123-45-6789",
  "employeeID": "EMP12345",
  "username": "support@empoweredbenefits.com",
  "gender": "F",
  "hireDate": {},
  "birthDate": {},
  "occupation": "tester579",
  "heightInFeet": 6,
  "heightInInch": 72,
  "weightInPounds": 200,
  "maritalStatus": "MARRIED",
  "tobaccoStatus": "UNDEFINED"
}
```

##Carriers 

###Get Carriers Incoming API

Retrieves a list of unique Carriers for a given Group number. If the service is unable to retrieve the list of unique Carriers, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error message.

Request url :
```
/api/groups/{groupNumber}/carriers/unique

```

##Plans

###Get Plans Incoming API

Retrieves active Plans given a specific Reference Date. If the service is unable to retrieve the active Plans, it will return a response with 400 status code and the response will also contain the appropriate errorCode and error m/api/groups/{groupNumber}/plans/{referenceDate}
essage.

Request url :
```
/api/groups/{groupNumber}/carriers/unique

```

