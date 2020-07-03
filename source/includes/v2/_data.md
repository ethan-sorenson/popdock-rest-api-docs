# Data

The Data endpoints can be used to retireve the data from any Popdock list. Samples of the different methods of retrieving the data is below.

There are 4 data endpoints available:

Name | Usage
--------- | ------- 
Get Entity Data | A simple quick method to pull the default fields 
Get Favorite Data | User friendly method to use the Popdock inteface to create endpoints
Get Endpoint Data | Building on Favorites by allowing custom parameters
Get Query Data | Most advanced method where the query is built at run-time

## Get Entity Data

Get data from the default fields on the 

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/data?format=json&company={{CompanyId}}</h6>
	</div>
</div>

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
format | false | Specifies the response format the available options are: csv, xml, json
company | true | Required field for which company to query
MaxRecords | false | Default MaxRecords is 100

<aside class="notice">
By default the endpoints only return 100 records. Only the default fields on the entity will be returned.
</aside>

> To retrieve a all data, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/data?format=json&company={{CompanyId}}" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/entity/{{EntityId}}/data?format=json&company={{CompanyId}}"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "Customernumber": "11728",
        "Name": "Fireworks OnTheRoof",
        "Balance": 0.00
    }
]
```
## Get Favorite Data

Get data returned from a favorite. This endpoint includes any customizations included in the favorite.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/favorite/{{FavoriteId}}/data?format=json</h6>
	</div>
</div>

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
format | false | Specifies the response format the available options are: csv, xml, json
MaxRecords | false | Default MaxRecords is 100

> To retrieve a all data, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/favorite/{{FavoriteId}}/data?format=json" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/favorite/{{FavoriteId}}/data?format=json"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "Customernumber": "11728",
        "Name": "Fireworks OnTheRoof",
        "Balance": 0.00
    }
]
```
## Get Endpoint Data

Get data returned from a an API endpoint as defined in the developer section of Popdock.

The main strength of this method is custom defined parameters can be used.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>https://{{ApiUrl}}/api/v2/favorite/TestApi?format=json&MaxRecords=10000&myParameter=myParameterValue</h6>
	</div>
</div>

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
format | false | Specifies the response format the available options are: csv, xml, json
MaxRecords | false | Default MaxRecords is 100

> To retrieve a all data, use this code:

```shell
curl GET "https://{{ApiUrl}}/api/v2/favorite/TestApi?format=json&MaxRecords=10000&myParameter=myParameterValue" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/favorite/TestApi?format=json&MaxRecords=10000&myParameter=myParameterValue"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}

response = requests.request("GET", url, headers=headers)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "Customernumber": "11728",
        "Name": "Fireworks OnTheRoof",
        "Balance": 0.00
    }
]
```
## Get Query Data

Query data while providing additional information 

The main strength of this method is flexibility. 

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">POST</i>
		<h6>https://{{ApiUrl}}/api/v2/query</h6>
	</div>
</div>

### Body Objects

The body of the query command contains 

Object | Type | Description
--------- | ------- | -----------
Id | GUID | Unique Identifier for the entity to use in the query
Format | String | Specifies the response format the available options are: csv, xml, json
Query | Object | Object contianing the query parameters
Fields | Array | List of fields to be returned by the query
Companies | Array | List of companies to include in the query
Restrictions | Array | List of restrictions
OrderBy | Array | List of fields to use for ordering the data
MaxRecords | Number | Specifies the maximum number of records returned

> To query for data, use this code:

```shell
curl POST "https://{{ApiUrl}}/api/v2/query" \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {{token}}'
  -d '{
	    "Id": "c9412916-32e2-4e51-bbe5-dc6e9422b74a",
	    "Format": "json",
	    "Query": {
		    "Fields": [
			    {
			    	"EntityFieldId": "b699b355-1b0e-4cdb-9cda-f2ccdc20418c"
			    },
			    {
			    	"EntityFieldId": "7e2f9774-cf1e-494c-801b-c0a67286f2ea"
			    }
		    ],
		    "Companies": [
		    	{
		    		"CompanyId": "06d0c3e3-b52f-47ae-a2c4-c379494805ea"
		    	},
		    	{
		    		"CompanyId": "a477ff7d-f9eb-4f3d-bc64-8d834f03ab93"
		    	}
	    	],
		    "Restrictions": [],
		    "OrderBy": [],
		    "MaxRecords": 10000
	    }
    }'
```

```python
import requests

url = "https://{{ApiUrl}}/api/v2/query"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {{token}}'
}
payload = 
{
	"Id": "c9412916-32e2-4e51-bbe5-dc6e9422b74a",
	"Format": "json",
	"Query": {
		"Fields": [
			{
				"EntityFieldId": "b699b355-1b0e-4cdb-9cda-f2ccdc20418c"
			},
			{
				"EntityFieldId": "7e2f9774-cf1e-494c-801b-c0a67286f2ea"
			}
		],
		"Companies": [
			{
				"CompanyId": "06d0c3e3-b52f-47ae-a2c4-c379494805ea"
			},
			{
				"CompanyId": "a477ff7d-f9eb-4f3d-bc64-8d834f03ab93"
			}
		],
		"Restrictions": [],
		"OrderBy": [],
		"MaxRecords": 10000
	}
}

response = requests.request("POST", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```
> The above command returns the following json:

```json
[
    {
        "Customernumber": "11728",
        "Name": "Fireworks OnTheRoof",
        "Balance": 0.00
    }
]
```