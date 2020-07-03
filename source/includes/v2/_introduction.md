# Introduction

Welcome to the Popdock API! The API can be used to remotely pull data from your Popodock Lists. Some of the core functions are:

* Retrieve lists of available connectors, lists, and favorites
* Query data from the list's data endpoints

## Requirements

To use this version of the REST API you will need the following:

* An active SaaS subscription for Popdock
* A valid user login to Popdock

## Getting Started

The Popdock API is locked by region, ensure the correct base url is used

Region | App Url | API Url
--------- | ------- | -----------
North America | data.popdock.com | api.popdock.com
Europe | data-weu.popdock.com | api-weu.popdock.com

# Authentication

The Popdock API uses user tokens for authentication. New authentication tokens can be geenrated in Popodock from any user's profile page.

The token will passed as a Bearer Token header with all api requests.

```json
{"error": "Invalid token"}
```

![User Token](images/User_Token.jpg)

<aside class="notice">
Tokens are user specific, they are the security equivalent of a user accessing the data through the Popdock web client.
</aside>

All data fields in Popdock are configured to a data type. These types are denoted by a type field.

Number | Type
--------- | -------
1 | String
2 | Date
3 | Currency
4 | Number
5 | Phone
6 | List
7 | Percentage
8 | Yes/no
9 | Time
10 | Quantity
11 | Email
12 | Website
13 | Image
14 | Skype
15 | Twitter
16 | 
17 | 
18 | Text
19 | GUID
20 | 
21 | Time span

## Errors

> Popdock REST API error example:

```json
{
    "Message": "An error has occurred.",
    "ExceptionMessage": "Invalid column name 'CustomEntityRestrictionId'.",
    "ExceptionType": "System.Data.SqlClient.SqlException",
    "StackTrace": "..."
}
```

The SmartConnect API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your API key is wrong.
404 | Not Found -- The resource you are looking for has been removed, or is temporarily unavailable.
500 | Internal Server Error -- We had a problem processing the request. Try again later.