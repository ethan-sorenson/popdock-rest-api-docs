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

## Errors

> Popdock REST API error example:

```json
{"error": "Invalid token"}
```

> Popdock REST API error example:

```json
{"error": "Favorite ID is missing or invalid"}
```

The SmartConnect API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your API key is wrong.
500 | Internal Server Error -- We had a problem processing the request. Try again later.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc/v3/coupons/&lt;id&gt;</h6>
	</div>
</div>